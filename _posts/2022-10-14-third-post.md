---
title: "opencv로 이미지 띄우기"
excerpt: "opencv를 이용해서 이미지 창을 띄우고 조절해보자"

categories:
- Blog
tags:
- [Blog, jekyll, opencv, image, Github, Git]

toc: true
toc_sticky: true

date: 2022-10-14
last_modified_at: 2022-10-14
---

''' python
import cv2
import os

def show_image(hr_path, predic_path, lr_path): # Load Images
    HR = cv2.imread(hr_path)  
    predict = cv2.imread(predict_path)
    LR_SRx4 = cv2.imread(lr_path)
    
    window_width = 640
    window_height = 480
    start_x = 0
    move_window_x = 500
    
    LR = cv2.resize(LR_SRx4, (0,0), fx=4, fy=4, interpolation=cv2.INTER_CUBIC)
    
    cv2.namedWindow('HR', cv2.WINDOW_NORMAL)
    cv2.namedWindow('predict', cv2.WINDOW_NORMAL)
    cv2.namedWindow('LR', cv2.WINDOW_NORMAL)
    cv2.resizeWindow('HR', window_height, window_width)
    cv2.resizeWindow('predict', window_height, window_width)
    cv2.resizeWindow('LR', window_height, window_width)
    cv2.moveWindow('HR', start_x, 0)
    cv2.moveWindow('predict', start_x + move_window_x, 0)
    cv2.moveWindow('LR', start_x + move_window_x*2, 0)
    
    cv2.imshow('HR', HR)
    cv2.imshow('predict', predict)
    cv2.imshow('LR', LR)
    cv2.waitKey(0)
    
if __name__ == "__main__":
    check_number = '????'
    iter = ????
    
    hr_path = './datasets/DIV2K/DIV2K_valid_HR/{}.png'.format(check_number)
    predict_path = './experiments/train_HAT_SRx4_from_scratch/visualization/{}/{}_{}.png'.format(check_number, check_number, iter)
    lr_path = './datasets/DIV2K/DIV2K_valid_LR_bicubic/{}.png'.format(check_number)
    
    show_image(hr_path, predict_path, lr_path)
'''

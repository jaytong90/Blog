---
layout: post
title: Activity了解其一
category: android基础
tags: android
keywords: android
description: 
---

# 1.Activity 生命周期

## 1.1 一般情况
### 启动Activity:
	 onCreate()——>onStart()——>onResume()【进入运行状态】
###  Activity退居后台：（当前Activity跳转到新的Activity,或者按住Home键）
	onPause()——> onStop() 【进入停滞状态】
### Activity返回前台：
	onRestart()——>onStart()——>onResume() 【 再次回到运行状态】
    
## 1.2特殊情况：    
### 正常启动:在此省略
###  Activity异常退居后台：
	【由于内存不足,系统![enter description here][1]会杀掉这个后台状态的Activity
    （此时该activity 任在任务栈中，但是activity引用指向的对象已经为null）】   
    onPause()—>onStop()——>onDestroy()
### Activity再次返回前台：
	走onCreate()–>onStart()—>onResume()(将重新走一次Activity的初始化生命周期)

### 锁屏：
	onPause()——> onStop()
### 解锁 :
	onStart()——> onResume()
## 1.3示意图

  [1]: ./images/activity%E7%94%9F%E5%91%BD%E5%91%A8%E6%9C%9F.png "activity生命周期.png"
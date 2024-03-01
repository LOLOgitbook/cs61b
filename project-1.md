# Project 1: Data Structures

## Introduction

目标：create two java files: LinkedListDeque.java 和 ArrayDeque.java

## Packages

完成2个packages，一个是Deque，一个是gh2。

package 是java classes 的一个集合，一起工作为了完成一个公共的目标。比如 org.junit是用来测试的， 其中的Assert class会使用，如果见到 org.junit.Assert.assertEquals，org.junit是package 的名字，Assert是class名字，assertEquals是method。We call `org.junit.Assert.assertEquals` the “canonical name” of the method, and we call `assertEquals` the “simple name” of the method.

如果code 是package的一部分，通过用package keyword。

`package deque;`

如果想用其中的class 或者 method，用import 让simple name 带入代码里。

## The Deque API

Deque ： double-ended queue

完成操作：

* public void addFirst(T item): 把类型T的项，加到队头。
* 。。。
* `public Iterator<T> iterator(）`Deque objects 是iterable。
* `public boolean equals(Object o)` 返回是否o是这个deque。

## Project Tasks

### 1. Linked List Deque

* create a file 叫 LinkedListDeque.java 在proj1/deque目录下，




























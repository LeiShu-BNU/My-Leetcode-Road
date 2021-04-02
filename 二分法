#题型一：二分求下标

#704 	二分查找（简单） 	
#35 	搜索插入位置（简单） 	【视频讲解】、文字题解
#34 	在排序数组中查找元素的第一个和最后一个位置（简单） 	【视频讲解】、文字题解
#1095 	山脉数组中查找目标值（中等） 	【视频讲解】、文字题解
#4 	寻找两个有序数组的中位数（困难） 	【视频讲解】、文字题解

#要看一下边界判断
#34
class Solution:
    def searchRange(self, nums: List[int], target: int) -> List[int]:
        size = len(nums)
        left , right = 0 , size
        while left < right:
            mid = int(left + (right - left)/2)
            if nums[mid] < target:
                left = mid+1
            elif nums[mid] == target:
                max_span = (right - left)//2+1
                start = mid-1
                end = mid+1
                while start >= 0 and nums[start] == target:
                    start -= 1
                while end <= size-1 and nums[end] == target:
                    end +=1
                return [start+1,end-1]
            else:
                right = mid
                
        return [-1,-1]

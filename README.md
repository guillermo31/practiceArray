# practiceArray
public int[] notAlone(int[] nums, int val) 
{
  int notAloneArray[] = new int[nums.length];
  
  for(int i = 0; i < notAloneArray.length; i++)
  {
    notAloneArray[i] = nums[i];
  }
  
  for(int i = 0; i < notAloneArray.length; i++)
  {
    for(i = 1; i < notAloneArray.length; i++)
    {
      if(notAloneArray[i] == val)
      {
        if(notAloneArray[i] < notAloneArray[i - 1])
        {
          notAloneArray[i] = notAloneArray[i - 1];
        }
        else if(notAloneArray[i] < notAloneArray[i + 1])
        {
          notAloneArray[i] = notAloneArray[i + 1];
        }
      }
    }
  }
  return notAloneArray;
  
}

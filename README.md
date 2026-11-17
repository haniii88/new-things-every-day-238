function dailyLog232() {
  const waterIntake = [250, 300, 200, 350, 250, 300];
  const dailyGoal = 2000;

  const totalIntake = waterIntake.reduce(
    (sum, amount) => sum + amount,
    0
  );

  const averagePerGlass = totalIntake / waterIntake.length;
  const progress = (totalIntake / dailyGoal) * 100;
  const remaining = Math.max(dailyGoal - totalIntake, 0);

  console.log("Daily Water Intake Report");
  console.log("-------------------------");
  console.log(`Total Intake: ${totalIntake} ml`);
  console.log(`Average per Glass: ${averagePerGlass.toFixed(1)} ml`);
  console.log(`Daily Goal: ${dailyGoal} ml`);
  console.log(`Progress: ${progress.toFixed(1)}%`);
  console.log(`Remaining: ${remaining} ml`);
}

dailyLog232();

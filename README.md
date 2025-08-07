function updateCountdown() {
  const now = new Date();
  const target = new Date('2024-01-01T00:00:00');
  if (now > target) target.setFullYear(target.getFullYear() + 1);

  const diff = target - now;

  const days = Math.floor(diff / (1000 * 60 * 60 * 24));
  const hours = Math.floor((diff / (1000 * 60 * 60)) % 24);
  const minutes = Math.floor((diff / (1000 * 60)) % 60);
  const seconds = Math.floor((diff / 1000) % 60);

  document.getElementById('days').textContent = days + ' روز';
  document.getElementById('hours').textContent = hours + ' ساعت';
  document.getElementById('minutes').textContent = minutes + ' دقیقه';
  document.getElementById('seconds').textContent = seconds + ' ثانیه';
}

// 프로필 링크 데이터 (예시)
const links = [
  {
    name: '💙 데이식스',
    url: 'https://search.naver.com/search.naver?where=nexearch&sm=top_sug.pre&fbm=0&acr=1&acq=epdl&qdt=0&ie=utf8&query=%EB%8D%B0%EC%9D%B4%EC%8B%9D%EC%8A%A4&ackey=vgs0o289',
  },
  {
    name: '🐱 고양이',
    url: 'https://search.naver.com/search.naver?ssc=tab.image.all&where=image&sm=tab_jum&query=%EA%B3%A0%EC%96%91%EC%9D%B4',
  },
  {
    name: '포트폴리오',
    url: 'https://your-portfolio.com/',
  },
  {
    name: '출생',
    url: 'mailto:honggildong@email.com',
  }
];

const list = document.getElementById('link-list');
links.forEach((link, idx) => {
  const li = document.createElement('li');
  if (link.name === '출생') {
    li.innerHTML = `<a class="profile-link" href="#" onclick="showBirth(event)">${link.name}</a>`;
  } else {
    li.innerHTML = `<a class="profile-link" href="${link.url}" target="_blank">${link.name}</a>`;
  }
  list.appendChild(li);
});

function showBirth(e) {
  e.preventDefault();
  alert('2008.05.11');
}

// 프로필 링크 복사
const copyBtn = document.getElementById('copy-link');
copyBtn.onclick = function() {
  navigator.clipboard.writeText(window.location.href);
  copyBtn.textContent = '복사됨!';
  setTimeout(() => (copyBtn.textContent = '프로필 링크 복사'), 1200);
};

// QR 코드 생성 및 모달 표시
const qrBtn = document.getElementById('show-qr');
const qrModal = document.getElementById('qr-modal');
const qrImg = document.getElementById('qr-img');
const closeQr = document.getElementById('close-qr');
qrBtn.onclick = function() {
  // 무료 QR API 사용 (goqr.me)
  qrImg.src = `https://api.qrserver.com/v1/create-qr-code/?size=180x180&data=${encodeURIComponent(window.location.href)}`;
  qrModal.style.display = 'block';
};
closeQr.onclick = function() {
  qrModal.style.display = 'none';
};
window.onclick = function(e) {
  if (e.target === qrModal) qrModal.style.display = 'none';
};

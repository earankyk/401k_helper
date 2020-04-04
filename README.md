# To 401k or not to 401k

As an immigrant in the US, I wasn't sure if I should invest my money in a tax advantaged account (401k/IRA) or an after tax brokerage account. It's a no-brainer to invest using a tax-advantaged account if you expect to be in the US by the time you're 65, however as immigrants on worker visas we rarely know if that's the case.  

Given this conundrum, an immigrant investor has two options:
* Invest using an after-tax brokerage account with the flexibility of being able to withdraw your money whenever you want.
* Invest using an IRA with pre-tax money knowing that you'd have to pay an early withdrawal penalty for a withdrawal before you turn 65.  

Each of these options also comes with it's own tax implications. In-order to aid my decision making, I built this webapp to compare the returns from investing the same amount of pre-tax money in a tax advantaged account vs an after-tax brokerage account.

<html lang="ja">
<head>
  <meta charset="UTF-8">
  <title>Tax Advantaged vs After Tax Returns</title>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.3.0/Chart.min.js"></script>
  <link rel="stylesheet" type="text/css" href="style.css">
</head>
<body onload="displayBarChart();">
  <div class="form-inline">
    <form>
      <label for="pre_tax_amount">Pre-tax investment amount (per year):</label><br>
      <input value=42000 id="pre_tax_amount" required><br>
      <label for="expected_cagr">Expected CAGR (%)</label><br>
      <input type="text" id="expected_cagr" value=7 required><br>
      <label for="contribution_limit">401k contribution limit</label><br>
      <input type="text" id="contribution_limit" value=19000 required><br>
      <label for="total_income_tax_rate">Income tax rate (%)</label><br>
      <input type="text" id="total_income_tax_rate" value=31 required><br>
      <label for="total_capital_gains_rate">Capital gains tax rate (%)</label><br>
      <input type="text" id="total_capital_gains_rate" value=21 required><br>
      <label for="early_withdrawal_penalty_rate">Early withdrawal penalty rate (%)</label><br>
      <input type="text" id="early_withdrawal_penalty_rate" value=10 required><br>
      <input type="button" value="Compare Returns" onclick="displayBarChart()">
    </form>
  </div>
  <div class="box">
    <canvas id="barChart" height="450" width="800"></canvas>
  </div>
  <script src="script.js"></script>
</body>
</html>
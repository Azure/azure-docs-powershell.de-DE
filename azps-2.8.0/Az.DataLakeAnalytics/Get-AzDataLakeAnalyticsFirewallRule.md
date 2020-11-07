---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 37c14547712233a025da56180e7a362f25168400
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651626"
---
# <span data-ttu-id="d095a-101">Get-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d095a-101">Get-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="d095a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d095a-102">SYNOPSIS</span></span>
<span data-ttu-id="d095a-103">Ruft eine Firewall-Regel oder eine Liste mit Firewallregeln aus einem Data Lake Analytics-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="d095a-103">Retrieves a firewall rule or list of firewall rules from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="d095a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d095a-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d095a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d095a-105">DESCRIPTION</span></span>
<span data-ttu-id="d095a-106">Das Cmdlet " **Get-AzDataLakeAnalyticsFirewallRule** " Ruft eine Firewall-Regel oder eine Liste mit Firewallregeln aus einem Azure Data Lake Analytics-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="d095a-106">The **Get-AzDataLakeAnalyticsFirewallRule** cmdlet retrieves a firewall rule or list of firewall rules from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="d095a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d095a-107">EXAMPLES</span></span>

### <span data-ttu-id="d095a-108">Beispiel 1: Abrufen einer Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="d095a-108">Example 1: Get a firewall rule</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="d095a-109">Dieser Befehl ruft die Firewall-Regel mit dem Namen "meine Firewall-Regel" aus dem Konto "ContosoAdlAcct" ab.</span><span class="sxs-lookup"><span data-stu-id="d095a-109">This command gets the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

### <span data-ttu-id="d095a-110">Beispiel 2: Auflisten aller Firewallregeln</span><span class="sxs-lookup"><span data-stu-id="d095a-110">Example 2: List all firewall rules</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct"
```

<span data-ttu-id="d095a-111">Dieser Befehl ruft alle Firewallregeln vom Konto "ContosoAdlAcct" ab.</span><span class="sxs-lookup"><span data-stu-id="d095a-111">This command gets all firewall rules from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="d095a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d095a-112">PARAMETERS</span></span>

### <span data-ttu-id="d095a-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="d095a-113">-Account</span></span>
<span data-ttu-id="d095a-114">Das Data Lake Analytics-Konto, aus dem die Firewall-Regel abgerufen werden soll</span><span class="sxs-lookup"><span data-stu-id="d095a-114">The Data Lake Analytics account to get the firewall rule from</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d095a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d095a-115">-DefaultProfile</span></span>
<span data-ttu-id="d095a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d095a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d095a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d095a-117">-Name</span></span>
<span data-ttu-id="d095a-118">Der Name der Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="d095a-118">The name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d095a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d095a-119">-ResourceGroupName</span></span>
<span data-ttu-id="d095a-120">Der Name der Ressourcengruppe, unter der das Konto abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d095a-120">Name of resource group under which want to retrieve the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d095a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d095a-121">CommonParameters</span></span>
<span data-ttu-id="d095a-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d095a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d095a-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d095a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d095a-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d095a-124">INPUTS</span></span>

### <span data-ttu-id="d095a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d095a-125">System.String</span></span>

## <span data-ttu-id="d095a-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d095a-126">OUTPUTS</span></span>

### <span data-ttu-id="d095a-127">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d095a-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="d095a-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="d095a-128">NOTES</span></span>

## <span data-ttu-id="d095a-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d095a-129">RELATED LINKS</span></span>

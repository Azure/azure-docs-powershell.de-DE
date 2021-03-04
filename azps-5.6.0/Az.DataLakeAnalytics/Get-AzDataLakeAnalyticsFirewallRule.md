---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: e95d29b5a91f8df257649693bdd9d4029ca3d166
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942803"
---
# <span data-ttu-id="27599-101">Get-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="27599-101">Get-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="27599-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27599-102">SYNOPSIS</span></span>
<span data-ttu-id="27599-103">Ruft eine Firewallregel oder eine Liste der Firewallregeln aus einem Data Lake Analytics-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="27599-103">Retrieves a firewall rule or list of firewall rules from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="27599-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27599-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27599-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27599-105">DESCRIPTION</span></span>
<span data-ttu-id="27599-106">Das **Get-AzDataLakeAnalyticsFirewallRule-Cmdlet** ruft eine Firewallregel oder eine Liste von Firewallregeln aus einem Azure Data Lake Analytics-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="27599-106">The **Get-AzDataLakeAnalyticsFirewallRule** cmdlet retrieves a firewall rule or list of firewall rules from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="27599-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="27599-107">EXAMPLES</span></span>

### <span data-ttu-id="27599-108">Beispiel 1: Erhalten einer Firewallregel</span><span class="sxs-lookup"><span data-stu-id="27599-108">Example 1: Get a firewall rule</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="27599-109">Dieser Befehl ruft die Firewallregel mit dem Namen "meine Firewallregel" aus dem Konto "ContosoAdlAcct" ab.</span><span class="sxs-lookup"><span data-stu-id="27599-109">This command gets the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

### <span data-ttu-id="27599-110">Beispiel 2: Auflisten aller Firewallregeln</span><span class="sxs-lookup"><span data-stu-id="27599-110">Example 2: List all firewall rules</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct"
```

<span data-ttu-id="27599-111">Dieser Befehl ruft alle Firewallregeln vom Konto "ContosoAdlAcct" ab.</span><span class="sxs-lookup"><span data-stu-id="27599-111">This command gets all firewall rules from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="27599-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="27599-112">PARAMETERS</span></span>

### <span data-ttu-id="27599-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="27599-113">-Account</span></span>
<span data-ttu-id="27599-114">Das Data Lake Analytics-Konto, aus dem die Firewallregel</span><span class="sxs-lookup"><span data-stu-id="27599-114">The Data Lake Analytics account to get the firewall rule from</span></span>

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

### <span data-ttu-id="27599-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27599-115">-DefaultProfile</span></span>
<span data-ttu-id="27599-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="27599-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27599-117">-Name</span><span class="sxs-lookup"><span data-stu-id="27599-117">-Name</span></span>
<span data-ttu-id="27599-118">Der Name der Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="27599-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="27599-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27599-119">-ResourceGroupName</span></span>
<span data-ttu-id="27599-120">Name der Ressourcengruppe, unter der das Konto abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="27599-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="27599-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27599-121">CommonParameters</span></span>
<span data-ttu-id="27599-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27599-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27599-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27599-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27599-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="27599-124">INPUTS</span></span>

### <span data-ttu-id="27599-125">System.String</span><span class="sxs-lookup"><span data-stu-id="27599-125">System.String</span></span>

## <span data-ttu-id="27599-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="27599-126">OUTPUTS</span></span>

### <span data-ttu-id="27599-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="27599-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="27599-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="27599-128">NOTES</span></span>

## <span data-ttu-id="27599-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="27599-129">RELATED LINKS</span></span>

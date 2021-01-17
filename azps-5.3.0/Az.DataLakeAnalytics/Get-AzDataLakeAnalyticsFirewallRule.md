---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 40c44ff157fca6a276cac8ece508e9d540b526ed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472613"
---
# <span data-ttu-id="f0fab-101">Get-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f0fab-101">Get-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="f0fab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0fab-102">SYNOPSIS</span></span>
<span data-ttu-id="f0fab-103">Ruft eine Firewallregel oder eine Liste der Firewallregeln aus einem Data Lake Analytics-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="f0fab-103">Retrieves a firewall rule or list of firewall rules from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="f0fab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f0fab-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0fab-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f0fab-105">DESCRIPTION</span></span>
<span data-ttu-id="f0fab-106">Das **Cmdlet "Get-AzDataLakeAnalyticsFirewallRule"** ruft eine Firewallregel oder eine Liste der Firewallregeln aus einem Azure Data Lake Analytics-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="f0fab-106">The **Get-AzDataLakeAnalyticsFirewallRule** cmdlet retrieves a firewall rule or list of firewall rules from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="f0fab-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f0fab-107">EXAMPLES</span></span>

### <span data-ttu-id="f0fab-108">Beispiel 1: Erhalten einer Firewallregel</span><span class="sxs-lookup"><span data-stu-id="f0fab-108">Example 1: Get a firewall rule</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="f0fab-109">Dieser Befehl ruft die Firewallregel mit dem Namen "Meine Firewallregel" aus dem Konto "ContosoAdlAcct" ab.</span><span class="sxs-lookup"><span data-stu-id="f0fab-109">This command gets the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

### <span data-ttu-id="f0fab-110">Beispiel 2: Auflisten aller Firewallregeln</span><span class="sxs-lookup"><span data-stu-id="f0fab-110">Example 2: List all firewall rules</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct"
```

<span data-ttu-id="f0fab-111">Dieser Befehl ruft alle Firewallregeln aus dem Konto "ContosoAdlAcct" ab.</span><span class="sxs-lookup"><span data-stu-id="f0fab-111">This command gets all firewall rules from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="f0fab-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0fab-112">PARAMETERS</span></span>

### <span data-ttu-id="f0fab-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="f0fab-113">-Account</span></span>
<span data-ttu-id="f0fab-114">Das Data Lake Analytics-Konto, von dem die Firewallregel erhalten werden soll</span><span class="sxs-lookup"><span data-stu-id="f0fab-114">The Data Lake Analytics account to get the firewall rule from</span></span>

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

### <span data-ttu-id="f0fab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0fab-115">-DefaultProfile</span></span>
<span data-ttu-id="f0fab-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f0fab-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0fab-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f0fab-117">-Name</span></span>
<span data-ttu-id="f0fab-118">Der Name der Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="f0fab-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="f0fab-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0fab-119">-ResourceGroupName</span></span>
<span data-ttu-id="f0fab-120">Name der Ressourcengruppe, unter der das Konto abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f0fab-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="f0fab-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0fab-121">CommonParameters</span></span>
<span data-ttu-id="f0fab-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0fab-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0fab-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0fab-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0fab-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f0fab-124">INPUTS</span></span>

### <span data-ttu-id="f0fab-125">System.String</span><span class="sxs-lookup"><span data-stu-id="f0fab-125">System.String</span></span>

## <span data-ttu-id="f0fab-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f0fab-126">OUTPUTS</span></span>

### <span data-ttu-id="f0fab-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f0fab-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="f0fab-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f0fab-128">NOTES</span></span>

## <span data-ttu-id="f0fab-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f0fab-129">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 56b1a9378914a7fa2220e948b64c357b06f6f4dc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472610"
---
# <span data-ttu-id="13013-101">Get-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="13013-101">Get-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="13013-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13013-102">SYNOPSIS</span></span>
<span data-ttu-id="13013-103">Ruft eine Data Lake Analytics-Berechnungsrichtlinie oder eine Liste von Berechnungsrichtlinien ab.</span><span class="sxs-lookup"><span data-stu-id="13013-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

## <span data-ttu-id="13013-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13013-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13013-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="13013-105">DESCRIPTION</span></span>
<span data-ttu-id="13013-106">Die **Get-AzDataLakeAnalyticsComputePolicy** ruft eine angegebene Azure Data Lake Analytics-Rechenrichtlinie oder eine Liste von Richtlinien ab.</span><span class="sxs-lookup"><span data-stu-id="13013-106">The **Get-AzDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="13013-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="13013-107">EXAMPLES</span></span>

### <span data-ttu-id="13013-108">Beispiel 1: Erhalten einer angegebenen Berechnungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="13013-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="13013-109">Dieser Befehl ruft die angegebene Berechnungsrichtlinie mit dem Namen "myPolicy" im Konto "contosoadla" ab.</span><span class="sxs-lookup"><span data-stu-id="13013-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="13013-110">Beispiel 2: Erhalten einer Liste aller Berechnungsrichtlinien im Konto</span><span class="sxs-lookup"><span data-stu-id="13013-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="13013-111">Dieser Befehl ruft eine Liste aller Berechnungsrichtlinien im Konto "contosoadla" ab.</span><span class="sxs-lookup"><span data-stu-id="13013-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="13013-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13013-112">PARAMETERS</span></span>

### <span data-ttu-id="13013-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="13013-113">-Account</span></span>
<span data-ttu-id="13013-114">Der Name des Kontos, von dem die Berechnungsrichtlinie bzw. die Berechnungsrichtlinien zu erhalten sind.</span><span class="sxs-lookup"><span data-stu-id="13013-114">Name of the account to get the compute policy or policies from.</span></span>

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

### <span data-ttu-id="13013-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13013-115">-DefaultProfile</span></span>
<span data-ttu-id="13013-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="13013-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13013-117">-Name</span><span class="sxs-lookup"><span data-stu-id="13013-117">-Name</span></span>
<span data-ttu-id="13013-118">Name der zu berechnende Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="13013-118">Name of the compute policy to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13013-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13013-119">-ResourceGroupName</span></span>
<span data-ttu-id="13013-120">Name der Ressourcengruppe, unter der Sie das Konto haben.</span><span class="sxs-lookup"><span data-stu-id="13013-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="13013-121">Optional und wird versucht zu ermitteln, wenn nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="13013-121">Optional and will attempt to discover if not provided.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13013-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13013-122">CommonParameters</span></span>
<span data-ttu-id="13013-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13013-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13013-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13013-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13013-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="13013-125">INPUTS</span></span>

### <span data-ttu-id="13013-126">System.String</span><span class="sxs-lookup"><span data-stu-id="13013-126">System.String</span></span>

## <span data-ttu-id="13013-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="13013-127">OUTPUTS</span></span>

### <span data-ttu-id="13013-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="13013-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="13013-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="13013-129">NOTES</span></span>

## <span data-ttu-id="13013-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="13013-130">RELATED LINKS</span></span>

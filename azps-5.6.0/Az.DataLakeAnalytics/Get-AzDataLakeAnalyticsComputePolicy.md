---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 6867e57e5465ddab8fc7f0adbfdb3197d8ac1245
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942811"
---
# <span data-ttu-id="30b9a-101">Get-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="30b9a-101">Get-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="30b9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30b9a-102">SYNOPSIS</span></span>
<span data-ttu-id="30b9a-103">Ruft eine Data Lake Analytics-Computerichtlinie oder eine Liste der Computerichtlinien ab.</span><span class="sxs-lookup"><span data-stu-id="30b9a-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

## <span data-ttu-id="30b9a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="30b9a-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30b9a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="30b9a-105">DESCRIPTION</span></span>
<span data-ttu-id="30b9a-106">Die **Get-AzDataLakeAnalyticsComputePolicy** ruft eine angegebene Azure Data Lake Analytics-Computerichtlinie oder eine Liste von Richtlinien ab.</span><span class="sxs-lookup"><span data-stu-id="30b9a-106">The **Get-AzDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="30b9a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="30b9a-107">EXAMPLES</span></span>

### <span data-ttu-id="30b9a-108">Beispiel 1: Erhalten einer angegebenen Computerichtlinie</span><span class="sxs-lookup"><span data-stu-id="30b9a-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="30b9a-109">Dieser Befehl ruft die angegebene Computerichtlinie mit dem Namen "myPolicy" im Konto "contosoadla" ab.</span><span class="sxs-lookup"><span data-stu-id="30b9a-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="30b9a-110">Beispiel 2: Erhalten einer Liste aller Computerichtlinien im Konto</span><span class="sxs-lookup"><span data-stu-id="30b9a-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="30b9a-111">Dieser Befehl ruft eine Liste aller Computerichtlinien im Konto "contosoadla" ab.</span><span class="sxs-lookup"><span data-stu-id="30b9a-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="30b9a-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="30b9a-112">PARAMETERS</span></span>

### <span data-ttu-id="30b9a-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="30b9a-113">-Account</span></span>
<span data-ttu-id="30b9a-114">Name des Kontos, aus dem die Datenverarbeitungsrichtlinie oder -richtlinie erhalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="30b9a-114">Name of the account to get the compute policy or policies from.</span></span>

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

### <span data-ttu-id="30b9a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30b9a-115">-DefaultProfile</span></span>
<span data-ttu-id="30b9a-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="30b9a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30b9a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="30b9a-117">-Name</span></span>
<span data-ttu-id="30b9a-118">Name der zu erhaltende Datenverarbeitungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="30b9a-118">Name of the compute policy to get.</span></span>

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

### <span data-ttu-id="30b9a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30b9a-119">-ResourceGroupName</span></span>
<span data-ttu-id="30b9a-120">Name der Ressourcengruppe, unter der Sie das Konto haben.</span><span class="sxs-lookup"><span data-stu-id="30b9a-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="30b9a-121">Optional und versucht zu ermitteln, wenn nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="30b9a-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="30b9a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30b9a-122">CommonParameters</span></span>
<span data-ttu-id="30b9a-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30b9a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30b9a-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30b9a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30b9a-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="30b9a-125">INPUTS</span></span>

### <span data-ttu-id="30b9a-126">System.String</span><span class="sxs-lookup"><span data-stu-id="30b9a-126">System.String</span></span>

## <span data-ttu-id="30b9a-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="30b9a-127">OUTPUTS</span></span>

### <span data-ttu-id="30b9a-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="30b9a-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="30b9a-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="30b9a-129">NOTES</span></span>

## <span data-ttu-id="30b9a-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="30b9a-130">RELATED LINKS</span></span>

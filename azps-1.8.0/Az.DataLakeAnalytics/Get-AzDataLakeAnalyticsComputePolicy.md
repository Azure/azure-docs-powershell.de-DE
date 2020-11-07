---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 776249a7a474e3918ed29003f631c984111ca25c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661307"
---
# <span data-ttu-id="3c057-101">Get-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="3c057-101">Get-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="3c057-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3c057-102">SYNOPSIS</span></span>
<span data-ttu-id="3c057-103">Ruft eine Data Lake Analytics-Compute-Richtlinie oder eine Liste der COMPUTE-Richtlinien ab.</span><span class="sxs-lookup"><span data-stu-id="3c057-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

## <span data-ttu-id="3c057-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c057-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c057-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3c057-105">DESCRIPTION</span></span>
<span data-ttu-id="3c057-106">Die **Get-AzDataLakeAnalyticsComputePolicy** Ruft eine angegebene Azure Data Lake Analytics-Berechnungs Richtlinie oder eine Liste mit Richtlinien ab.</span><span class="sxs-lookup"><span data-stu-id="3c057-106">The **Get-AzDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="3c057-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3c057-107">EXAMPLES</span></span>

### <span data-ttu-id="3c057-108">Beispiel 1: Abrufen einer angegebenen Compute-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="3c057-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="3c057-109">Dieser Befehl ruft die angegebene Compute-Richtlinie mit dem Namen "meine Richtlinie" im Konto "contosoadla" ab.</span><span class="sxs-lookup"><span data-stu-id="3c057-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="3c057-110">Beispiel 2: Abrufen einer Liste aller Compute-Richtlinien im Konto</span><span class="sxs-lookup"><span data-stu-id="3c057-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="3c057-111">Dieser Befehl ruft eine Liste aller Compute-Richtlinien im Konto "contosoadla" ab.</span><span class="sxs-lookup"><span data-stu-id="3c057-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="3c057-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c057-112">PARAMETERS</span></span>

### <span data-ttu-id="3c057-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="3c057-113">-Account</span></span>
<span data-ttu-id="3c057-114">Der Name des Kontos, von dem die Compute-Richtlinie oder Richtlinien abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3c057-114">Name of the account to get the compute policy or policies from.</span></span>

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

### <span data-ttu-id="3c057-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c057-115">-DefaultProfile</span></span>
<span data-ttu-id="3c057-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3c057-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c057-117">-Name</span><span class="sxs-lookup"><span data-stu-id="3c057-117">-Name</span></span>
<span data-ttu-id="3c057-118">Der Name der abzurufenden Compute-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="3c057-118">Name of the compute policy to get.</span></span>

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

### <span data-ttu-id="3c057-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c057-119">-ResourceGroupName</span></span>
<span data-ttu-id="3c057-120">Name der Ressourcengruppe, unter der Sie das Konto vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="3c057-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="3c057-121">Optional und versucht, festzustellen, wenn Sie nicht bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3c057-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="3c057-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c057-122">CommonParameters</span></span>
<span data-ttu-id="3c057-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c057-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c057-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c057-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c057-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3c057-125">INPUTS</span></span>

### <span data-ttu-id="3c057-126">System. String</span><span class="sxs-lookup"><span data-stu-id="3c057-126">System.String</span></span>

## <span data-ttu-id="3c057-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3c057-127">OUTPUTS</span></span>

### <span data-ttu-id="3c057-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="3c057-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="3c057-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="3c057-129">NOTES</span></span>

## <span data-ttu-id="3c057-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3c057-130">RELATED LINKS</span></span>

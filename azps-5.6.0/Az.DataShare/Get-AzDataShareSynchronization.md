---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharesynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
ms.openlocfilehash: a4d3adbcc63eda80bced31523a43cbbad4513205
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938187"
---
# <span data-ttu-id="cd723-101">Get-AzDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="cd723-101">Get-AzDataShareSynchronization</span></span>

## <span data-ttu-id="cd723-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd723-102">SYNOPSIS</span></span>
<span data-ttu-id="cd723-103">Ruft Informationen zur Synchronisierungseinstellung für eine Freigabe ab.</span><span class="sxs-lookup"><span data-stu-id="cd723-103">Gets information about synchronization setting for a share.</span></span>

## <span data-ttu-id="cd723-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd723-104">SYNTAX</span></span>

### <span data-ttu-id="cd723-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="cd723-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronization -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd723-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd723-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cd723-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cd723-107">DESCRIPTION</span></span>
<span data-ttu-id="cd723-108">Das **Get-AzDataShareSynchronization-Cmdlet** enthält Informationen zu allen Synchronisierungseinstellungen, die in einer Freigabe unter einem Datenfreigabekonto vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="cd723-108">The **Get-AzDataShareSynchronization** cmdlet provides information about all the synchronization setting present in a share under a data share account.</span></span>

## <span data-ttu-id="cd723-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cd723-109">EXAMPLES</span></span>

### <span data-ttu-id="cd723-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cd723-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare"

Company           : ADS Test
DurationMs        : 107013
EndTime           : 7/8/2019 11:53:18 PM
Message           :
StartTime         : 7/8/2019 11:51:34 PM
Status            : Succeeded
SynchronizationId : e6dc7080-6589-4628-8b50-8fc31b460089
```

<span data-ttu-id="cd723-111">Diese Befehle enthalten Informationen zu allen Synchronisierungseinstellungen, die in Share AdsShare im WikiAds des Datenfreigabekontos vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="cd723-111">This commands provides information about all synchronization settings present in share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="cd723-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="cd723-112">PARAMETERS</span></span>

### <span data-ttu-id="cd723-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cd723-113">-AccountName</span></span>
<span data-ttu-id="cd723-114">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="cd723-114">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd723-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd723-115">-DefaultProfile</span></span>
<span data-ttu-id="cd723-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd723-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd723-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd723-117">-ResourceGroupName</span></span>
<span data-ttu-id="cd723-118">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="cd723-118">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd723-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd723-119">-ResourceId</span></span>
<span data-ttu-id="cd723-120">Azure Data Share Resource ID</span><span class="sxs-lookup"><span data-stu-id="cd723-120">Azure data share resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd723-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="cd723-121">-ShareName</span></span>
<span data-ttu-id="cd723-122">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="cd723-122">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd723-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd723-123">CommonParameters</span></span>
<span data-ttu-id="cd723-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd723-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd723-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd723-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd723-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cd723-126">INPUTS</span></span>

### <span data-ttu-id="cd723-127">System.String</span><span class="sxs-lookup"><span data-stu-id="cd723-127">System.String</span></span>

## <span data-ttu-id="cd723-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cd723-128">OUTPUTS</span></span>

### <span data-ttu-id="cd723-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="cd723-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span></span>

## <span data-ttu-id="cd723-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="cd723-130">NOTES</span></span>

## <span data-ttu-id="cd723-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="cd723-131">RELATED LINKS</span></span>

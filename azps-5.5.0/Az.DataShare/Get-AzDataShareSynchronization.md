---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
ms.openlocfilehash: b60b43b2c0a28be969ad633c80338f42b2c98db6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148068"
---
# <span data-ttu-id="60492-101">Get-AzDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="60492-101">Get-AzDataShareSynchronization</span></span>

## <span data-ttu-id="60492-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60492-102">SYNOPSIS</span></span>
<span data-ttu-id="60492-103">Ruft Informationen zur Synchronisierungseinstellung für eine Freigabe ab.</span><span class="sxs-lookup"><span data-stu-id="60492-103">Gets information about synchronization setting for a share.</span></span>

## <span data-ttu-id="60492-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60492-104">SYNTAX</span></span>

### <span data-ttu-id="60492-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="60492-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronization -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60492-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="60492-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="60492-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60492-107">DESCRIPTION</span></span>
<span data-ttu-id="60492-108">Das **Cmdlet "Get-AzDataShareSynchronization"** enthält Informationen zu allen Synchronisierungseinstellungen, die in einer Freigabe unter einem Datenfreigabekonto vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="60492-108">The **Get-AzDataShareSynchronization** cmdlet provides information about all the synchronization setting present in a share under a data share account.</span></span>

## <span data-ttu-id="60492-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="60492-109">EXAMPLES</span></span>

### <span data-ttu-id="60492-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="60492-110">Example 1</span></span>
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

<span data-ttu-id="60492-111">Diese Befehle enthalten Informationen zu allen Synchronisierungseinstellungen, die in "Teilen von AdsShare" im WikiAds des Datenfreigabekontos vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="60492-111">This commands provides information about all synchronization settings present in share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="60492-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60492-112">PARAMETERS</span></span>

### <span data-ttu-id="60492-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="60492-113">-AccountName</span></span>
<span data-ttu-id="60492-114">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="60492-114">Azure data share account name</span></span>

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

### <span data-ttu-id="60492-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60492-115">-DefaultProfile</span></span>
<span data-ttu-id="60492-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60492-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60492-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60492-117">-ResourceGroupName</span></span>
<span data-ttu-id="60492-118">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="60492-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="60492-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60492-119">-ResourceId</span></span>
<span data-ttu-id="60492-120">Azure Data Share Resource ID</span><span class="sxs-lookup"><span data-stu-id="60492-120">Azure data share resource id</span></span>

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

### <span data-ttu-id="60492-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="60492-121">-ShareName</span></span>
<span data-ttu-id="60492-122">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="60492-122">Azure data share name</span></span>

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

### <span data-ttu-id="60492-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60492-123">CommonParameters</span></span>
<span data-ttu-id="60492-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60492-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60492-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60492-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60492-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="60492-126">INPUTS</span></span>

### <span data-ttu-id="60492-127">System.String</span><span class="sxs-lookup"><span data-stu-id="60492-127">System.String</span></span>

## <span data-ttu-id="60492-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="60492-128">OUTPUTS</span></span>

### <span data-ttu-id="60492-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="60492-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span></span>

## <span data-ttu-id="60492-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="60492-130">NOTES</span></span>

## <span data-ttu-id="60492-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="60492-131">RELATED LINKS</span></span>

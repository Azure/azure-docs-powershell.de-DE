---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 183164c3f2a18e68b9eab3f505f382a161abf415
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377360"
---
# <span data-ttu-id="d1d34-101">Get-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="d1d34-101">Get-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="d1d34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1d34-102">SYNOPSIS</span></span>
<span data-ttu-id="d1d34-103">Ruft Informationen zur Synchronisierungseinstellung für eine Freigabe ab.</span><span class="sxs-lookup"><span data-stu-id="d1d34-103">Gets information about synchronization setting on a share.</span></span>

## <span data-ttu-id="d1d34-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d1d34-104">SYNTAX</span></span>

### <span data-ttu-id="d1d34-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d1d34-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1d34-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1d34-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1d34-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d1d34-107">DESCRIPTION</span></span>
<span data-ttu-id="d1d34-108">Das **Cmdlet "Get-AzDataShareSynchronizationSetting"** enthält Informationen zur auf einer Freigabe aktivierten Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="d1d34-108">The **Get-AzDataShareSynchronizationSetting** cmdlet provides information about synchronization enabled on a share.</span></span> 

## <span data-ttu-id="d1d34-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d1d34-109">EXAMPLES</span></span>

### <span data-ttu-id="d1d34-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d1d34-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ShareSynchronization"

RecurrenceInterval  : Day
SynchronizationTime : 7/9/2019 9:00:00 AM
ProvisioningState   : Succeeded
CreatedAt           : 7/10/2019 12:01:08 AM
CreatedBy           : ADS Test
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.
                      DataShare/accounts/WikiAds/shares/AdShare/synchronizationSettings/ShareSynchronization
Name                : ShareSynchronization
Type                : Microsoft.DataShare/SynchronizationSettings
```

<span data-ttu-id="d1d34-111">Dieser Befehl enthält Informationen zur Synchronisierung, die für die Freigabe von AdsShare unter den WikiAds des Datenfreigabekontos aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d1d34-111">This command provides information about synchronization ShareSynchronization enabled on share AdsShare under data share account WikiAds.</span></span>

## <span data-ttu-id="d1d34-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1d34-112">PARAMETERS</span></span>

### <span data-ttu-id="d1d34-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d1d34-113">-AccountName</span></span>
<span data-ttu-id="d1d34-114">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="d1d34-114">Azure data share account name</span></span>

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

### <span data-ttu-id="d1d34-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1d34-115">-DefaultProfile</span></span>
<span data-ttu-id="d1d34-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1d34-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1d34-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d1d34-117">-Name</span></span>
<span data-ttu-id="d1d34-118">Name für Synchronisierungseinstellung</span><span class="sxs-lookup"><span data-stu-id="d1d34-118">Name for Synchronization Setting</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1d34-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1d34-119">-ResourceGroupName</span></span>
<span data-ttu-id="d1d34-120">Ressourcengruppenname des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="d1d34-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="d1d34-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1d34-121">-ResourceId</span></span>
<span data-ttu-id="d1d34-122">Die Ressourcen-ID der Einstellung für die Synchronisierung der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="d1d34-122">The resource id of the azure data share synchronization setting</span></span>

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

### <span data-ttu-id="d1d34-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="d1d34-123">-ShareName</span></span>
<span data-ttu-id="d1d34-124">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="d1d34-124">Azure data share name</span></span>

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

### <span data-ttu-id="d1d34-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1d34-125">CommonParameters</span></span>
<span data-ttu-id="d1d34-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1d34-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1d34-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1d34-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1d34-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d1d34-128">INPUTS</span></span>

### <span data-ttu-id="d1d34-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d1d34-129">System.String</span></span>

## <span data-ttu-id="d1d34-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d1d34-130">OUTPUTS</span></span>

### <span data-ttu-id="d1d34-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="d1d34-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="d1d34-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d1d34-132">NOTES</span></span>

## <span data-ttu-id="d1d34-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d1d34-133">RELATED LINKS</span></span>

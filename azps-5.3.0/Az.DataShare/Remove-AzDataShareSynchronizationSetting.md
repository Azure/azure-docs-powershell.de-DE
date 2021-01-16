---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 04454028957dfee3c7d50c47341be7e979ed3a9f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377095"
---
# <span data-ttu-id="8b387-101">Remove-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="8b387-101">Remove-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="8b387-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b387-102">SYNOPSIS</span></span>
<span data-ttu-id="8b387-103">Entfernt eine Synchronisierungseinstellung</span><span class="sxs-lookup"><span data-stu-id="8b387-103">removes a synchronization setting</span></span>

## <span data-ttu-id="8b387-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b387-104">SYNTAX</span></span>

### <span data-ttu-id="8b387-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8b387-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b387-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b387-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b387-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b387-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -InputObject <PSDataShareSynchronizationSetting> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b387-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b387-108">DESCRIPTION</span></span>
<span data-ttu-id="8b387-109">Das **Cmdlet "Remove-AzDataShareSynchronizationSetting"** entfernt eine Einstellung für die Datenfreigabesynchronisierung.</span><span class="sxs-lookup"><span data-stu-id="8b387-109">The **Remove-AzDataShareSynchronizationSetting** cmdlet removes a datashare synchronization setting</span></span>

## <span data-ttu-id="8b387-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8b387-110">EXAMPLES</span></span>

### <span data-ttu-id="8b387-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8b387-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsShareSynchronizationSetting"

Are you sure you want to remove synchronization-setting "AdsShareSynchronizationSetting"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="8b387-112">Mit diesen Befehlen wird eine Synchronisierungseinstellung namens AdsShareSynchronizationSetting aus der Freigabe von AdsShare entfernt.</span><span class="sxs-lookup"><span data-stu-id="8b387-112">This commands removes a synchronization setting named AdsShareSynchronizationSetting from share AdsShare.</span></span> 

## <span data-ttu-id="8b387-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b387-113">PARAMETERS</span></span>

### <span data-ttu-id="8b387-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8b387-114">-AccountName</span></span>
<span data-ttu-id="8b387-115">Azure Data Share Account Name</span><span class="sxs-lookup"><span data-stu-id="8b387-115">Azure Data Share Account name</span></span>

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

### <span data-ttu-id="8b387-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b387-116">-AsJob</span></span>
<span data-ttu-id="8b387-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="8b387-117">{{Fill AsJob Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b387-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b387-118">-DefaultProfile</span></span>
<span data-ttu-id="8b387-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8b387-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b387-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b387-120">-InputObject</span></span>
<span data-ttu-id="8b387-121">Die Einstellung für die Synchronisierung der Azure-Datenfreigabe.</span><span class="sxs-lookup"><span data-stu-id="8b387-121">The Azure Data Share Synchronization setting.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b387-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8b387-122">-Name</span></span>
<span data-ttu-id="8b387-123">Name der Synchronisierungseinstellung</span><span class="sxs-lookup"><span data-stu-id="8b387-123">Synchronization setting name</span></span>

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

### <span data-ttu-id="8b387-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b387-124">-PassThru</span></span>
<span data-ttu-id="8b387-125">Rückgabeobjekt (sofern angegeben)</span><span class="sxs-lookup"><span data-stu-id="8b387-125">Return object (if specified).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b387-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b387-126">-ResourceGroupName</span></span>
<span data-ttu-id="8b387-127">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="8b387-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="8b387-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b387-128">-ResourceId</span></span>
<span data-ttu-id="8b387-129">Die Ressourcen-ID der Synchronisierungseinstellung</span><span class="sxs-lookup"><span data-stu-id="8b387-129">The resource id of the synchronization setting</span></span>

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

### <span data-ttu-id="8b387-130">-ShareName</span><span class="sxs-lookup"><span data-stu-id="8b387-130">-ShareName</span></span>
<span data-ttu-id="8b387-131">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="8b387-131">Azure data share name</span></span>

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

### <span data-ttu-id="8b387-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b387-132">-Confirm</span></span>
<span data-ttu-id="8b387-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8b387-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b387-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8b387-134">-WhatIf</span></span>
<span data-ttu-id="8b387-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8b387-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b387-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8b387-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b387-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b387-137">CommonParameters</span></span>
<span data-ttu-id="8b387-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b387-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b387-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b387-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b387-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8b387-140">INPUTS</span></span>

### <span data-ttu-id="8b387-141">System.String</span><span class="sxs-lookup"><span data-stu-id="8b387-141">System.String</span></span>

### <span data-ttu-id="8b387-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="8b387-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="8b387-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8b387-143">OUTPUTS</span></span>

### <span data-ttu-id="8b387-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8b387-144">System.Boolean</span></span>

## <span data-ttu-id="8b387-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8b387-145">NOTES</span></span>

## <span data-ttu-id="8b387-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8b387-146">RELATED LINKS</span></span>

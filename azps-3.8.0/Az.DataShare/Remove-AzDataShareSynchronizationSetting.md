---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: b460054009afed75c58dfa092c2004193856d98d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004626"
---
# <span data-ttu-id="d22c0-101">Remove-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="d22c0-101">Remove-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="d22c0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d22c0-102">SYNOPSIS</span></span>
<span data-ttu-id="d22c0-103">entfernt eine Synchronisierungseinstellung.</span><span class="sxs-lookup"><span data-stu-id="d22c0-103">removes a synchronization setting</span></span>

## <span data-ttu-id="d22c0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d22c0-104">SYNTAX</span></span>

### <span data-ttu-id="d22c0-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d22c0-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d22c0-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d22c0-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d22c0-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d22c0-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -InputObject <PSDataShareSynchronizationSetting> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d22c0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d22c0-108">DESCRIPTION</span></span>
<span data-ttu-id="d22c0-109">Das Cmdlet " **Remove-AzDataShareSynchronizationSetting** " entfernt eine DataShare-Synchronisierungseinstellung.</span><span class="sxs-lookup"><span data-stu-id="d22c0-109">The **Remove-AzDataShareSynchronizationSetting** cmdlet removes a datashare synchronization setting</span></span>

## <span data-ttu-id="d22c0-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d22c0-110">EXAMPLES</span></span>

### <span data-ttu-id="d22c0-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d22c0-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsShareSynchronizationSetting"

Are you sure you want to remove synchronization-setting "AdsShareSynchronizationSetting"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="d22c0-112">Mit diesen Befehlen wird eine Synchronisierungseinstellung mit dem Namen AdsShareSynchronizationSetting aus Freigabe AdsShare entfernt.</span><span class="sxs-lookup"><span data-stu-id="d22c0-112">This commands removes a synchronization setting named AdsShareSynchronizationSetting from share AdsShare.</span></span> 

## <span data-ttu-id="d22c0-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d22c0-113">PARAMETERS</span></span>

### <span data-ttu-id="d22c0-114">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="d22c0-114">-AccountName</span></span>
<span data-ttu-id="d22c0-115">Name des Azure-Datenfreigabe Kontos</span><span class="sxs-lookup"><span data-stu-id="d22c0-115">Azure Data Share Account name</span></span>

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

### <span data-ttu-id="d22c0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d22c0-116">-AsJob</span></span>
<span data-ttu-id="d22c0-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="d22c0-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="d22c0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d22c0-118">-DefaultProfile</span></span>
<span data-ttu-id="d22c0-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d22c0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d22c0-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d22c0-120">-InputObject</span></span>
<span data-ttu-id="d22c0-121">Die Azure Data Share-Synchronisierungseinstellung.</span><span class="sxs-lookup"><span data-stu-id="d22c0-121">The Azure Data Share Synchronization setting.</span></span>


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

### <span data-ttu-id="d22c0-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d22c0-122">-Name</span></span>
<span data-ttu-id="d22c0-123">Name der Synchronisierungseinstellung</span><span class="sxs-lookup"><span data-stu-id="d22c0-123">Synchronization setting name</span></span>

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

### <span data-ttu-id="d22c0-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d22c0-124">-PassThru</span></span>
<span data-ttu-id="d22c0-125">Objekt zurückgeben (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="d22c0-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="d22c0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d22c0-126">-ResourceGroupName</span></span>
<span data-ttu-id="d22c0-127">Der Name der Ressourcengruppe des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="d22c0-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="d22c0-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d22c0-128">-ResourceId</span></span>
<span data-ttu-id="d22c0-129">Die Ressourcen-ID der Synchronisierungseinstellung</span><span class="sxs-lookup"><span data-stu-id="d22c0-129">The resource id of the synchronization setting</span></span>

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

### <span data-ttu-id="d22c0-130">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="d22c0-130">-ShareName</span></span>
<span data-ttu-id="d22c0-131">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="d22c0-131">Azure data share name</span></span>

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

### <span data-ttu-id="d22c0-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d22c0-132">-Confirm</span></span>
<span data-ttu-id="d22c0-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d22c0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d22c0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d22c0-134">-WhatIf</span></span>
<span data-ttu-id="d22c0-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d22c0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d22c0-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d22c0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d22c0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d22c0-137">CommonParameters</span></span>
<span data-ttu-id="d22c0-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d22c0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d22c0-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d22c0-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d22c0-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d22c0-140">INPUTS</span></span>

### <span data-ttu-id="d22c0-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d22c0-141">System.String</span></span>

### <span data-ttu-id="d22c0-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="d22c0-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="d22c0-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d22c0-143">OUTPUTS</span></span>

### <span data-ttu-id="d22c0-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d22c0-144">System.Boolean</span></span>

## <span data-ttu-id="d22c0-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="d22c0-145">NOTES</span></span>

## <span data-ttu-id="d22c0-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d22c0-146">RELATED LINKS</span></span>

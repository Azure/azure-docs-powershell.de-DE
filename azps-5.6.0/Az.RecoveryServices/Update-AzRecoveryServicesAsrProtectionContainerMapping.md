---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 29c996036705e3fc71f1c6a04ead16c24b1b3bca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918115"
---
# <span data-ttu-id="97b4c-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="97b4c-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="97b4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97b4c-102">SYNOPSIS</span></span>
<span data-ttu-id="97b4c-103">Aktualisieren Sie die Containerzuordnung für den Azure-Websitewiederherstellungsschutz.</span><span class="sxs-lookup"><span data-stu-id="97b4c-103">Update the Azure site recovery protection container mapping.</span></span>

## <span data-ttu-id="97b4c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97b4c-104">SYNTAX</span></span>

### <span data-ttu-id="97b4c-105">AzureToAzureEnableAutoUpdate (Standard)</span><span class="sxs-lookup"><span data-stu-id="97b4c-105">AzureToAzureEnableAutoUpdate (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-EnableAutoUpdate] -AutomationAccountId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97b4c-106">AzureToAzureDisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="97b4c-106">AzureToAzureDisableAutoUpdate</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-DisableAutoUpdate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="97b4c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="97b4c-107">DESCRIPTION</span></span>
<span data-ttu-id="97b4c-108">Das **Cmdlet Update-AzRecoveryServicesAsrProtectionContainerMapping** aktualisiert die angegebene Azure Site Recovery Protection-Containerzuordnung.</span><span class="sxs-lookup"><span data-stu-id="97b4c-108">The **Update-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet updates the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="97b4c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="97b4c-109">EXAMPLES</span></span>

### <span data-ttu-id="97b4c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="97b4c-110">Example 1</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping -AzureToAzure -DisableAutoUpdate
```

<span data-ttu-id="97b4c-111">Starten Sie den Vorgang, um die automatische Aktualisierung für Container zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="97b4c-111">Start the operation to disable auto update for container.</span></span>

### <span data-ttu-id="97b4c-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="97b4c-112">Example 2</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping  -AzureToAzure -EnableAutoUpdate -AutomationAccountId $automationAccountId
```

<span data-ttu-id="97b4c-113">Starten Sie den Vorgang, um die automatische Aktualisierung für Container zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="97b4c-113">Start the operation to disable enable auto update for container.</span></span>

## <span data-ttu-id="97b4c-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="97b4c-114">PARAMETERS</span></span>

### <span data-ttu-id="97b4c-115">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="97b4c-115">-AutomationAccountId</span></span>
<span data-ttu-id="97b4c-116">Gibt das AutomatisierungskontoId an, das für die automatische Udpate verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="97b4c-116">Specifies the automation accountId used for auto udpate.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureEnableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b4c-117">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="97b4c-117">-AzureToAzure</span></span>
<span data-ttu-id="97b4c-118">Gibt den Azure-zu-Azure-Schutzcontainer an.</span><span class="sxs-lookup"><span data-stu-id="97b4c-118">Specifies Azure to Azure protection container.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b4c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97b4c-119">-DefaultProfile</span></span>
<span data-ttu-id="97b4c-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="97b4c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97b4c-121">-DisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="97b4c-121">-DisableAutoUpdate</span></span>
<span data-ttu-id="97b4c-122">Parameter wechseln, um die automatische Aktualisierung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="97b4c-122">Switch parameter to disable auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureDisableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b4c-123">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="97b4c-123">-EnableAutoUpdate</span></span>
<span data-ttu-id="97b4c-124">Parameter wechseln, um die automatische Aktualisierung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="97b4c-124">Switch parameter to enable auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureEnableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b4c-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97b4c-125">-InputObject</span></span>
<span data-ttu-id="97b4c-126">Objekt für die Schutzcontainerzuordnung.</span><span class="sxs-lookup"><span data-stu-id="97b4c-126">Object for protection container mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97b4c-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="97b4c-127">-Confirm</span></span>
<span data-ttu-id="97b4c-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="97b4c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97b4c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97b4c-129">-WhatIf</span></span>
<span data-ttu-id="97b4c-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="97b4c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97b4c-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="97b4c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97b4c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97b4c-132">CommonParameters</span></span>
<span data-ttu-id="97b4c-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97b4c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97b4c-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97b4c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97b4c-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="97b4c-135">INPUTS</span></span>

### <span data-ttu-id="97b4c-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="97b4c-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="97b4c-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="97b4c-137">OUTPUTS</span></span>

### <span data-ttu-id="97b4c-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="97b4c-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="97b4c-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="97b4c-139">NOTES</span></span>

## <span data-ttu-id="97b4c-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="97b4c-140">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 49c3fa6ec85f97c3c4010b6cfc9282933a844a6e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160049"
---
# <span data-ttu-id="6906f-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="6906f-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="6906f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6906f-102">SYNOPSIS</span></span>
<span data-ttu-id="6906f-103">Aktualisieren Sie die Containerzuordnung für den Azure-Websitewiederherstellungsschutz.</span><span class="sxs-lookup"><span data-stu-id="6906f-103">Update the Azure site recovery protection container mapping.</span></span>

## <span data-ttu-id="6906f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6906f-104">SYNTAX</span></span>

### <span data-ttu-id="6906f-105">AzureToAzureEnableAutoUpdate (Standard)</span><span class="sxs-lookup"><span data-stu-id="6906f-105">AzureToAzureEnableAutoUpdate (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-EnableAutoUpdate] -AutomationAccountId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6906f-106">AzureToAzureDisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="6906f-106">AzureToAzureDisableAutoUpdate</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-DisableAutoUpdate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6906f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6906f-107">DESCRIPTION</span></span>
<span data-ttu-id="6906f-108">Das **Cmdlet "Update-AzRecoveryServicesAsrProtectionContainerMapping"** aktualisiert die angegebene Azure Site Recovery Protection-Containerzuordnung.</span><span class="sxs-lookup"><span data-stu-id="6906f-108">The **Update-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet updates the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="6906f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6906f-109">EXAMPLES</span></span>

### <span data-ttu-id="6906f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6906f-110">Example 1</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping -AzureToAzure -DisableAutoUpdate
```

<span data-ttu-id="6906f-111">Starten Sie den Vorgang, um die automatische Aktualisierung für Container zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="6906f-111">Start the operation to disable auto update for container.</span></span>

### <span data-ttu-id="6906f-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6906f-112">Example 2</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping  -AzureToAzure -EnableAutoUpdate -AutomationAccountId $automationAccountId
```

<span data-ttu-id="6906f-113">Starten Sie den Vorgang, um die automatische Aktualisierung für Container zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="6906f-113">Start the operation to disable enable auto update for container.</span></span>

## <span data-ttu-id="6906f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6906f-114">PARAMETERS</span></span>

### <span data-ttu-id="6906f-115">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="6906f-115">-AutomationAccountId</span></span>
<span data-ttu-id="6906f-116">Gibt die automatisierungskonto-ID an, die für die automatische Verwendung von Benutzerdefinierten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6906f-116">Specifies the automation accountId used for auto udpate.</span></span>

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

### <span data-ttu-id="6906f-117">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="6906f-117">-AzureToAzure</span></span>
<span data-ttu-id="6906f-118">Gibt den Container "Azure-zu-Azure-Schutz" an.</span><span class="sxs-lookup"><span data-stu-id="6906f-118">Specifies Azure to Azure protection container.</span></span>

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

### <span data-ttu-id="6906f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6906f-119">-DefaultProfile</span></span>
<span data-ttu-id="6906f-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6906f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6906f-121">-DisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="6906f-121">-DisableAutoUpdate</span></span>
<span data-ttu-id="6906f-122">Parameter wechseln, um die automatische Aktualisierung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="6906f-122">Switch parameter to disable auto update.</span></span>

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

### <span data-ttu-id="6906f-123">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="6906f-123">-EnableAutoUpdate</span></span>
<span data-ttu-id="6906f-124">Parameter wechseln, um die automatische Aktualisierung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="6906f-124">Switch parameter to enable auto update.</span></span>

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

### <span data-ttu-id="6906f-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6906f-125">-InputObject</span></span>
<span data-ttu-id="6906f-126">Objekt für die Schutzcontainerzuordnung.</span><span class="sxs-lookup"><span data-stu-id="6906f-126">Object for protection container mapping.</span></span>

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

### <span data-ttu-id="6906f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6906f-127">-Confirm</span></span>
<span data-ttu-id="6906f-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6906f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6906f-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6906f-129">-WhatIf</span></span>
<span data-ttu-id="6906f-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6906f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6906f-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6906f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6906f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6906f-132">CommonParameters</span></span>
<span data-ttu-id="6906f-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6906f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6906f-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6906f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6906f-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6906f-135">INPUTS</span></span>

### <span data-ttu-id="6906f-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="6906f-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="6906f-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6906f-137">OUTPUTS</span></span>

### <span data-ttu-id="6906f-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="6906f-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6906f-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6906f-139">NOTES</span></span>

## <span data-ttu-id="6906f-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6906f-140">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 49c3fa6ec85f97c3c4010b6cfc9282933a844a6e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995509"
---
# <span data-ttu-id="84373-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="84373-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="84373-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="84373-102">SYNOPSIS</span></span>
<span data-ttu-id="84373-103">Aktualisieren Sie die Container Zuordnung für Azure Site Recovery Protection.</span><span class="sxs-lookup"><span data-stu-id="84373-103">Update the Azure site recovery protection container mapping.</span></span>

## <span data-ttu-id="84373-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="84373-104">SYNTAX</span></span>

### <span data-ttu-id="84373-105">AzureToAzureEnableAutoUpdate (Standard)</span><span class="sxs-lookup"><span data-stu-id="84373-105">AzureToAzureEnableAutoUpdate (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-EnableAutoUpdate] -AutomationAccountId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84373-106">AzureToAzureDisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="84373-106">AzureToAzureDisableAutoUpdate</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-DisableAutoUpdate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="84373-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="84373-107">DESCRIPTION</span></span>
<span data-ttu-id="84373-108">Das Cmdlet **Update-AzRecoveryServicesAsrProtectionContainerMapping** aktualisiert die angegebene Azure Site Recovery Protection-Container Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="84373-108">The **Update-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet updates the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="84373-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="84373-109">EXAMPLES</span></span>

### <span data-ttu-id="84373-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="84373-110">Example 1</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping -AzureToAzure -DisableAutoUpdate
```

<span data-ttu-id="84373-111">Starten Sie den Vorgang, um die automatische Aktualisierung für Container zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="84373-111">Start the operation to disable auto update for container.</span></span>

### <span data-ttu-id="84373-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="84373-112">Example 2</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping  -AzureToAzure -EnableAutoUpdate -AutomationAccountId $automationAccountId
```

<span data-ttu-id="84373-113">Starten Sie den Vorgang, um automatisches Update für Container aktivieren zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="84373-113">Start the operation to disable enable auto update for container.</span></span>

## <span data-ttu-id="84373-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="84373-114">PARAMETERS</span></span>

### <span data-ttu-id="84373-115">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="84373-115">-AutomationAccountId</span></span>
<span data-ttu-id="84373-116">Gibt die Automatisierungs-Konto-Nr an, die für die automatische UDPATE verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="84373-116">Specifies the automation accountId used for auto udpate.</span></span>

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

### <span data-ttu-id="84373-117">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="84373-117">-AzureToAzure</span></span>
<span data-ttu-id="84373-118">Gibt den Azure-to-Azure-Schutzcontainer an.</span><span class="sxs-lookup"><span data-stu-id="84373-118">Specifies Azure to Azure protection container.</span></span>

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

### <span data-ttu-id="84373-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84373-119">-DefaultProfile</span></span>
<span data-ttu-id="84373-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="84373-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84373-121">-DisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="84373-121">-DisableAutoUpdate</span></span>
<span data-ttu-id="84373-122">Parameter wechseln, um die automatische Aktualisierung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="84373-122">Switch parameter to disable auto update.</span></span>

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

### <span data-ttu-id="84373-123">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="84373-123">-EnableAutoUpdate</span></span>
<span data-ttu-id="84373-124">Parameter wechseln, um die automatische Aktualisierung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="84373-124">Switch parameter to enable auto update.</span></span>

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

### <span data-ttu-id="84373-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="84373-125">-InputObject</span></span>
<span data-ttu-id="84373-126">Objekt für Schutzcontainer Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="84373-126">Object for protection container mapping.</span></span>

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

### <span data-ttu-id="84373-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="84373-127">-Confirm</span></span>
<span data-ttu-id="84373-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="84373-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84373-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84373-129">-WhatIf</span></span>
<span data-ttu-id="84373-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="84373-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84373-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="84373-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84373-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84373-132">CommonParameters</span></span>
<span data-ttu-id="84373-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84373-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84373-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84373-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84373-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="84373-135">INPUTS</span></span>

### <span data-ttu-id="84373-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="84373-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="84373-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="84373-137">OUTPUTS</span></span>

### <span data-ttu-id="84373-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="84373-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="84373-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="84373-139">NOTES</span></span>

## <span data-ttu-id="84373-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="84373-140">RELATED LINKS</span></span>

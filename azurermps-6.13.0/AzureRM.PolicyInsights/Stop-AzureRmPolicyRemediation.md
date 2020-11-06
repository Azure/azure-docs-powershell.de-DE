---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/stop-azurermpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Stop-AzureRmPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Stop-AzureRmPolicyRemediation.md
ms.openlocfilehash: 6e36b2ce8fb03173bfaab80b68c219873875526c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480206"
---
# <span data-ttu-id="71424-101">Stop-AzureRmPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="71424-101">Stop-AzureRmPolicyRemediation</span></span>

## <span data-ttu-id="71424-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="71424-102">SYNOPSIS</span></span>
<span data-ttu-id="71424-103">Bricht eine in-Progress-Richtlinien Bereinigung ab.</span><span class="sxs-lookup"><span data-stu-id="71424-103">Cancels an in-progress policy remediation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71424-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="71424-104">SYNTAX</span></span>

### <span data-ttu-id="71424-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="71424-105">ByName (Default)</span></span>
```
Stop-AzureRmPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71424-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="71424-106">ByResourceId</span></span>
```
Stop-AzureRmPolicyRemediation -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71424-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="71424-107">ByInputObject</span></span>
```
Stop-AzureRmPolicyRemediation -InputObject <PSRemediation> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71424-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71424-108">DESCRIPTION</span></span>
<span data-ttu-id="71424-109">Das Cmdlet " **Stop-AzureRmPolicyRemediation** " bricht eine in-Progress-Richtlinien Bereinigung ab.</span><span class="sxs-lookup"><span data-stu-id="71424-109">The **Stop-AzureRmPolicyRemediation** cmdlet cancels an in-progress policy remediation.</span></span> <span data-ttu-id="71424-110">Aktive Bereitstellungen werden abgebrochen, und es werden keine neuen Bereitstellungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="71424-110">Active deployments will be canceled and no new deployments will be created.</span></span>

## <span data-ttu-id="71424-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="71424-111">EXAMPLES</span></span>

### <span data-ttu-id="71424-112">Beispiel 1: Abbrechen einer Richtlinien Bereinigung im Bereich der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="71424-112">Example 1: Cancel a policy remediation at resource group scope</span></span>
```
PS C:\> Stop-AzureRmPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="71424-113">Mit diesem Befehl wird die Bereinigung mit dem Namen "remediation1" in der Ressourcengruppe "myRG" abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="71424-113">This command cancels the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="71424-114">Beispiel 2: Abbrechen einer Verwaltungsgruppen Bereinigung über Rohre</span><span class="sxs-lookup"><span data-stu-id="71424-114">Example 2: Cancel a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzureRmPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Stop-AzureRmPolicyRemediation
```

<span data-ttu-id="71424-115">Mit diesem Befehl wird die Bereinigung mit dem Namen "remediation1" in der Verwaltungsgruppe "mg1" abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="71424-115">This command cancels the remediation named 'remediation1' in management group 'mg1'.</span></span>

## <span data-ttu-id="71424-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="71424-116">PARAMETERS</span></span>

### <span data-ttu-id="71424-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71424-117">-AsJob</span></span>
<span data-ttu-id="71424-118">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="71424-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="71424-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71424-119">-DefaultProfile</span></span>
<span data-ttu-id="71424-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="71424-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71424-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="71424-121">-InputObject</span></span>
<span data-ttu-id="71424-122">Das Behebungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="71424-122">The Remediation object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71424-123">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="71424-123">-ManagementGroupName</span></span>
<span data-ttu-id="71424-124">Verwaltungsgruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="71424-124">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71424-125">-Name</span><span class="sxs-lookup"><span data-stu-id="71424-125">-Name</span></span>
<span data-ttu-id="71424-126">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="71424-126">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71424-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71424-127">-PassThru</span></span>
<span data-ttu-id="71424-128">Gibt "true" zurück, wenn der Befehl erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="71424-128">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="71424-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71424-129">-ResourceGroupName</span></span>
<span data-ttu-id="71424-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="71424-130">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71424-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="71424-131">-ResourceId</span></span>
<span data-ttu-id="71424-132">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="71424-132">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71424-133">-Scope</span><span class="sxs-lookup"><span data-stu-id="71424-133">-Scope</span></span>
<span data-ttu-id="71424-134">Der Bereich der Ressource.</span><span class="sxs-lookup"><span data-stu-id="71424-134">Scope of the resource.</span></span>
<span data-ttu-id="71424-135">Z.b..</span><span class="sxs-lookup"><span data-stu-id="71424-135">E.g.</span></span>
<span data-ttu-id="71424-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="71424-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71424-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="71424-137">-Confirm</span></span>
<span data-ttu-id="71424-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="71424-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71424-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71424-139">-WhatIf</span></span>
<span data-ttu-id="71424-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="71424-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71424-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="71424-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71424-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71424-142">CommonParameters</span></span>
<span data-ttu-id="71424-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71424-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71424-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71424-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71424-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="71424-145">INPUTS</span></span>

### <span data-ttu-id="71424-146">System. String</span><span class="sxs-lookup"><span data-stu-id="71424-146">System.String</span></span>

### <span data-ttu-id="71424-147">Microsoft. Azure. Commands. PolicyInsights. Models. Remediation. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="71424-147">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="71424-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="71424-148">OUTPUTS</span></span>

### <span data-ttu-id="71424-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="71424-149">System.Boolean</span></span>

## <span data-ttu-id="71424-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="71424-150">NOTES</span></span>

## <span data-ttu-id="71424-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="71424-151">RELATED LINKS</span></span>

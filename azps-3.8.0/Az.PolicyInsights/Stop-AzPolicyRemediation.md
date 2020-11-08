---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/stop-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
ms.openlocfilehash: 9dfb3ff2f50df7a858ab8194ec86fa312501dcff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995371"
---
# <span data-ttu-id="b256c-101">Stop-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="b256c-101">Stop-AzPolicyRemediation</span></span>

## <span data-ttu-id="b256c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b256c-102">SYNOPSIS</span></span>
<span data-ttu-id="b256c-103">Bricht eine in-Progress-Richtlinien Bereinigung ab.</span><span class="sxs-lookup"><span data-stu-id="b256c-103">Cancels an in-progress policy remediation.</span></span>

## <span data-ttu-id="b256c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b256c-104">SYNTAX</span></span>

### <span data-ttu-id="b256c-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b256c-105">ByName (Default)</span></span>
```
Stop-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b256c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b256c-106">ByResourceId</span></span>
```
Stop-AzPolicyRemediation -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b256c-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b256c-107">ByInputObject</span></span>
```
Stop-AzPolicyRemediation -InputObject <PSRemediation> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b256c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b256c-108">DESCRIPTION</span></span>
<span data-ttu-id="b256c-109">Das Cmdlet " **Stop-AzPolicyRemediation** " bricht eine in-Progress-Richtlinien Bereinigung ab.</span><span class="sxs-lookup"><span data-stu-id="b256c-109">The **Stop-AzPolicyRemediation** cmdlet cancels an in-progress policy remediation.</span></span> <span data-ttu-id="b256c-110">Aktive Bereitstellungen werden abgebrochen, und es werden keine neuen Bereitstellungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="b256c-110">Active deployments will be canceled and no new deployments will be created.</span></span>

## <span data-ttu-id="b256c-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b256c-111">EXAMPLES</span></span>

### <span data-ttu-id="b256c-112">Beispiel 1: Abbrechen einer Richtlinien Bereinigung im Bereich der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="b256c-112">Example 1: Cancel a policy remediation at resource group scope</span></span>
```
PS C:\> Stop-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="b256c-113">Mit diesem Befehl wird die Bereinigung mit dem Namen "remediation1" in der Ressourcengruppe "myRG" abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="b256c-113">This command cancels the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="b256c-114">Beispiel 2: Abbrechen einer Verwaltungsgruppen Bereinigung über Rohre</span><span class="sxs-lookup"><span data-stu-id="b256c-114">Example 2: Cancel a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Stop-AzPolicyRemediation
```

<span data-ttu-id="b256c-115">Mit diesem Befehl wird die Bereinigung mit dem Namen "remediation1" in der Verwaltungsgruppe "mg1" abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="b256c-115">This command cancels the remediation named 'remediation1' in management group 'mg1'.</span></span>

## <span data-ttu-id="b256c-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="b256c-116">PARAMETERS</span></span>

### <span data-ttu-id="b256c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b256c-117">-AsJob</span></span>
<span data-ttu-id="b256c-118">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="b256c-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="b256c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b256c-119">-DefaultProfile</span></span>
<span data-ttu-id="b256c-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b256c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b256c-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b256c-121">-InputObject</span></span>
<span data-ttu-id="b256c-122">Das Behebungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="b256c-122">The Remediation object.</span></span>

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

### <span data-ttu-id="b256c-123">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="b256c-123">-ManagementGroupName</span></span>
<span data-ttu-id="b256c-124">Verwaltungsgruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="b256c-124">Management group ID.</span></span>

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

### <span data-ttu-id="b256c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b256c-125">-Name</span></span>
<span data-ttu-id="b256c-126">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="b256c-126">Resource name.</span></span>

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

### <span data-ttu-id="b256c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b256c-127">-PassThru</span></span>
<span data-ttu-id="b256c-128">Gibt "true" zurück, wenn der Befehl erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="b256c-128">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="b256c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b256c-129">-ResourceGroupName</span></span>
<span data-ttu-id="b256c-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b256c-130">Resource group name.</span></span>

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

### <span data-ttu-id="b256c-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b256c-131">-ResourceId</span></span>
<span data-ttu-id="b256c-132">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b256c-132">Resource ID.</span></span>

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

### <span data-ttu-id="b256c-133">-Scope</span><span class="sxs-lookup"><span data-stu-id="b256c-133">-Scope</span></span>
<span data-ttu-id="b256c-134">Der Bereich der Ressource.</span><span class="sxs-lookup"><span data-stu-id="b256c-134">Scope of the resource.</span></span>
<span data-ttu-id="b256c-135">Z.b..</span><span class="sxs-lookup"><span data-stu-id="b256c-135">E.g.</span></span>
<span data-ttu-id="b256c-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="b256c-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="b256c-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b256c-137">-Confirm</span></span>
<span data-ttu-id="b256c-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b256c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b256c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b256c-139">-WhatIf</span></span>
<span data-ttu-id="b256c-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b256c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b256c-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b256c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b256c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b256c-142">CommonParameters</span></span>
<span data-ttu-id="b256c-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b256c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b256c-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b256c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b256c-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b256c-145">INPUTS</span></span>

### <span data-ttu-id="b256c-146">System. String</span><span class="sxs-lookup"><span data-stu-id="b256c-146">System.String</span></span>

### <span data-ttu-id="b256c-147">Microsoft. Azure. Commands. PolicyInsights. Models. Remediation. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="b256c-147">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="b256c-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b256c-148">OUTPUTS</span></span>

### <span data-ttu-id="b256c-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b256c-149">System.Boolean</span></span>

## <span data-ttu-id="b256c-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="b256c-150">NOTES</span></span>

## <span data-ttu-id="b256c-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b256c-151">RELATED LINKS</span></span>

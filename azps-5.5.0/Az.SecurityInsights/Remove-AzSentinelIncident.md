---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelIncident.md
ms.openlocfilehash: faf2c40bc43c1b42861bc93d2398d4d26731c112
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165116"
---
# <span data-ttu-id="576e3-101">Remove-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="576e3-101">Remove-AzSentinelIncident</span></span>

## <span data-ttu-id="576e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="576e3-102">SYNOPSIS</span></span>
<span data-ttu-id="576e3-103">Löschen eines Vorfalls</span><span class="sxs-lookup"><span data-stu-id="576e3-103">Delete an Incident.</span></span>

## <span data-ttu-id="576e3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="576e3-104">SYNTAX</span></span>

### <span data-ttu-id="576e3-105">IncidentId (Standard)</span><span class="sxs-lookup"><span data-stu-id="576e3-105">IncidentId (Default)</span></span>
```
Remove-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="576e3-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="576e3-106">InputObject</span></span>
```
Remove-AzSentinelIncident -InputObject <PSSentinelIncident> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="576e3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="576e3-107">DESCRIPTION</span></span>
<span data-ttu-id="576e3-108">Das **Cmdlet "Remove-AzSentinelIncident"** löscht einen Vorfall endgültig aus einem angegebenen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="576e3-108">The **Remove-AzSentinelIncident** cmdlet permanently deletes a Incident from a specified workspace.</span></span>
<span data-ttu-id="576e3-109">Sie können ein **Vorfallobjekt** mithilfe des Pipelineoperators übergeben, oder Sie können die erforderlichen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="576e3-109">You can pass an **Incident** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="576e3-110">Sie können den Parameter "Bestätigen" und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="576e3-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="576e3-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="576e3-111">EXAMPLES</span></span>

### <span data-ttu-id="576e3-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="576e3-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="576e3-113">Mit diesem Befehl wird der Vorfall aus dem Arbeitsbereich entfernt.</span><span class="sxs-lookup"><span data-stu-id="576e3-113">This command removes the Incident from the workspace.</span></span>

## <span data-ttu-id="576e3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="576e3-114">PARAMETERS</span></span>

### <span data-ttu-id="576e3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="576e3-115">-DefaultProfile</span></span>
<span data-ttu-id="576e3-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="576e3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="576e3-117">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="576e3-117">-IncidentId</span></span>
<span data-ttu-id="576e3-118">Vorfall-ID.</span><span class="sxs-lookup"><span data-stu-id="576e3-118">Incident Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="576e3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="576e3-119">-InputObject</span></span>
<span data-ttu-id="576e3-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="576e3-120">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="576e3-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="576e3-121">-PassThru</span></span>
<span data-ttu-id="576e3-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="576e3-122">PassThru</span></span>

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

### <span data-ttu-id="576e3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="576e3-123">-ResourceGroupName</span></span>
<span data-ttu-id="576e3-124">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="576e3-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="576e3-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="576e3-125">-WorkspaceName</span></span>
<span data-ttu-id="576e3-126">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="576e3-126">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="576e3-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="576e3-127">-Confirm</span></span>
<span data-ttu-id="576e3-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="576e3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="576e3-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="576e3-129">-WhatIf</span></span>
<span data-ttu-id="576e3-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="576e3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="576e3-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="576e3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="576e3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="576e3-132">CommonParameters</span></span>
<span data-ttu-id="576e3-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="576e3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="576e3-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="576e3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="576e3-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="576e3-135">INPUTS</span></span>

### <span data-ttu-id="576e3-136">System.String</span><span class="sxs-lookup"><span data-stu-id="576e3-136">System.String</span></span>
### <span data-ttu-id="576e3-137">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="576e3-137">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="576e3-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="576e3-138">OUTPUTS</span></span>

### <span data-ttu-id="576e3-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="576e3-139">System.Boolean</span></span>
## <span data-ttu-id="576e3-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="576e3-140">NOTES</span></span>

## <span data-ttu-id="576e3-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="576e3-141">RELATED LINKS</span></span>

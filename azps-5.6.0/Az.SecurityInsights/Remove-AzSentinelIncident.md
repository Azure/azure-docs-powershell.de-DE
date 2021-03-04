---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/remove-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelIncident.md
ms.openlocfilehash: 80badb2e73aa00fd9a221c20372ab42499c1cb0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927563"
---
# <span data-ttu-id="a018e-101">Remove-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="a018e-101">Remove-AzSentinelIncident</span></span>

## <span data-ttu-id="a018e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a018e-102">SYNOPSIS</span></span>
<span data-ttu-id="a018e-103">Löschen eines Vorfalls</span><span class="sxs-lookup"><span data-stu-id="a018e-103">Delete an Incident.</span></span>

## <span data-ttu-id="a018e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a018e-104">SYNTAX</span></span>

### <span data-ttu-id="a018e-105">IncidentId (Standard)</span><span class="sxs-lookup"><span data-stu-id="a018e-105">IncidentId (Default)</span></span>
```
Remove-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a018e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a018e-106">InputObject</span></span>
```
Remove-AzSentinelIncident -InputObject <PSSentinelIncident> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a018e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a018e-107">DESCRIPTION</span></span>
<span data-ttu-id="a018e-108">Das **Cmdlet Remove-AzSentinelIncident** löscht einen Vorfall endgültig aus einem angegebenen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="a018e-108">The **Remove-AzSentinelIncident** cmdlet permanently deletes a Incident from a specified workspace.</span></span>
<span data-ttu-id="a018e-109">Sie können ein **Incident-Objekt** mithilfe des Pipelineoperators übergeben oder die erforderlichen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="a018e-109">You can pass an **Incident** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="a018e-110">Sie können den Parameter Bestätigen und die $ConfirmPreference Windows PowerShell verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="a018e-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="a018e-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a018e-111">EXAMPLES</span></span>

### <span data-ttu-id="a018e-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a018e-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="a018e-113">Mit diesem Befehl wird der Vorfall aus dem Arbeitsbereich entfernt.</span><span class="sxs-lookup"><span data-stu-id="a018e-113">This command removes the Incident from the workspace.</span></span>

## <span data-ttu-id="a018e-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a018e-114">PARAMETERS</span></span>

### <span data-ttu-id="a018e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a018e-115">-DefaultProfile</span></span>
<span data-ttu-id="a018e-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a018e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a018e-117">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="a018e-117">-IncidentId</span></span>
<span data-ttu-id="a018e-118">Vorfall-ID.</span><span class="sxs-lookup"><span data-stu-id="a018e-118">Incident Id.</span></span>

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

### <span data-ttu-id="a018e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a018e-119">-InputObject</span></span>
<span data-ttu-id="a018e-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="a018e-120">InputObject.</span></span>

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

### <span data-ttu-id="a018e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a018e-121">-PassThru</span></span>
<span data-ttu-id="a018e-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="a018e-122">PassThru</span></span>

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

### <span data-ttu-id="a018e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a018e-123">-ResourceGroupName</span></span>
<span data-ttu-id="a018e-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a018e-124">Resource group name.</span></span>

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

### <span data-ttu-id="a018e-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a018e-125">-WorkspaceName</span></span>
<span data-ttu-id="a018e-126">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="a018e-126">Workspace Name.</span></span>

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

### <span data-ttu-id="a018e-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a018e-127">-Confirm</span></span>
<span data-ttu-id="a018e-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a018e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a018e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a018e-129">-WhatIf</span></span>
<span data-ttu-id="a018e-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a018e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a018e-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a018e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a018e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a018e-132">CommonParameters</span></span>
<span data-ttu-id="a018e-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a018e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a018e-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a018e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a018e-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a018e-135">INPUTS</span></span>

### <span data-ttu-id="a018e-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a018e-136">System.String</span></span>
### <span data-ttu-id="a018e-137">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="a018e-137">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="a018e-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a018e-138">OUTPUTS</span></span>

### <span data-ttu-id="a018e-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a018e-139">System.Boolean</span></span>
## <span data-ttu-id="a018e-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a018e-140">NOTES</span></span>

## <span data-ttu-id="a018e-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a018e-141">RELATED LINKS</span></span>

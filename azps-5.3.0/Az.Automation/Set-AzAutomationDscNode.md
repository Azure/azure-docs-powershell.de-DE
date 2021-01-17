---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 60023C8D-EA37-41DA-97E6-AF89F7F9BADD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationDscNode.md
ms.openlocfilehash: 02a6d7a129dc084b982f1827d678354265ddbc66
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471253"
---
# <span data-ttu-id="3a076-101">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="3a076-101">Set-AzAutomationDscNode</span></span>

## <span data-ttu-id="3a076-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a076-102">SYNOPSIS</span></span>
<span data-ttu-id="3a076-103">Ändert die Knotenkonfiguration, der ein DSC-Knoten zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3a076-103">Modifies the node configuration that a DSC node is mapped to.</span></span>

## <span data-ttu-id="3a076-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a076-104">SYNTAX</span></span>

```
Set-AzAutomationDscNode -Id <Guid> -NodeConfigurationName <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3a076-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3a076-105">DESCRIPTION</span></span>
<span data-ttu-id="3a076-106">Das **Cmdlet "Set-AzAutomationDscNode"** ändert eine Konfiguration des Knotens "APS Desired State Configuration (DSC)".</span><span class="sxs-lookup"><span data-stu-id="3a076-106">The **Set-AzAutomationDscNode** cmdlet modifies an APS Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="3a076-107">Azure Automation speichert die KONFIGURATION von DSC-Knoten als Konfigurationsdokument für verwaltetes Objektformat (Managed Object Format, MOF).</span><span class="sxs-lookup"><span data-stu-id="3a076-107">Azure Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="3a076-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3a076-108">EXAMPLES</span></span>

### <span data-ttu-id="3a076-109">Beispiel 1: Ändern der Knotenkonfigurationszuordnung</span><span class="sxs-lookup"><span data-stu-id="3a076-109">Example 1: Modify node configuration mapping</span></span>
```
PS C:\>Set-AzAutomationDscNode -NodeConfigurationName "Contoso.NodeConfiguration01" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111c8a6067j8
```

<span data-ttu-id="3a076-110">Dieser Befehl weist dem Knoten mit der angegebenen GUID die Knotenkonfiguration "Contoso.NodeConfiguration01" zu.</span><span class="sxs-lookup"><span data-stu-id="3a076-110">This command assigns the node configuration named Contoso.NodeConfiguration01 to the node that has the specified GUID.</span></span>

## <span data-ttu-id="3a076-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a076-111">PARAMETERS</span></span>

### <span data-ttu-id="3a076-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3a076-112">-AutomationAccountName</span></span>
<span data-ttu-id="3a076-113">Gibt den Namen des Automatisierungskontos an, das den DSC-Knoten enthält, für den dieses Cmdlet die Konfiguration ändert.</span><span class="sxs-lookup"><span data-stu-id="3a076-113">Specifies the name of the Automation account that contains the DSC node for which this cmdlet modifies the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a076-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a076-114">-DefaultProfile</span></span>
<span data-ttu-id="3a076-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="3a076-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a076-116">-Force</span><span class="sxs-lookup"><span data-stu-id="3a076-116">-Force</span></span>
<span data-ttu-id="3a076-117">ps_force sie den Befehl, der ausgeführt werden soll, ohne dass der Benutzer zur Bestätigung des Benutzers aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="3a076-117">ps_force the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3a076-118">-ID</span><span class="sxs-lookup"><span data-stu-id="3a076-118">-Id</span></span>
<span data-ttu-id="3a076-119">Gibt die eindeutige ID des DSC-Knotens an, für den dieses Cmdlet die Konfiguration ändert.</span><span class="sxs-lookup"><span data-stu-id="3a076-119">Specifies the unique ID of the DSC node for which this cmdlet modifies the configuration.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a076-120">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="3a076-120">-NodeConfigurationName</span></span>
<span data-ttu-id="3a076-121">Gibt den Namen der Knotenkonfiguration an, der dieses Cmdlet den Knoten zu ordnet.</span><span class="sxs-lookup"><span data-stu-id="3a076-121">Specifies the name of the node configuration to which this cmdlet maps the node.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a076-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a076-122">-ResourceGroupName</span></span>
<span data-ttu-id="3a076-123">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet eine DSC-Knotenkonfiguration ändert.</span><span class="sxs-lookup"><span data-stu-id="3a076-123">Specifies the name of a resource group in which this cmdlet modifies a DSC node configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a076-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a076-124">-Confirm</span></span>
<span data-ttu-id="3a076-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3a076-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a076-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3a076-126">-WhatIf</span></span>
<span data-ttu-id="3a076-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3a076-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a076-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3a076-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a076-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a076-129">CommonParameters</span></span>
<span data-ttu-id="3a076-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a076-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a076-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a076-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a076-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3a076-132">INPUTS</span></span>

### <span data-ttu-id="3a076-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="3a076-133">System.Guid</span></span>

### <span data-ttu-id="3a076-134">System.String</span><span class="sxs-lookup"><span data-stu-id="3a076-134">System.String</span></span>

## <span data-ttu-id="3a076-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3a076-135">OUTPUTS</span></span>

### <span data-ttu-id="3a076-136">Microsoft.Azure.Commands.Automation.Model.Dscnode</span><span class="sxs-lookup"><span data-stu-id="3a076-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="3a076-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3a076-137">NOTES</span></span>

## <span data-ttu-id="3a076-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3a076-138">RELATED LINKS</span></span>

[<span data-ttu-id="3a076-139">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="3a076-139">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="3a076-140">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="3a076-140">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="3a076-141">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="3a076-141">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 60023C8D-EA37-41DA-97E6-AF89F7F9BADD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationDscNode.md
ms.openlocfilehash: 2b0d6096e9691445c939daea113dcdac2fa6c5fd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93657944"
---
# <span data-ttu-id="9229b-101">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="9229b-101">Set-AzAutomationDscNode</span></span>

## <span data-ttu-id="9229b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9229b-102">SYNOPSIS</span></span>
<span data-ttu-id="9229b-103">Ändert die Knoten Konfiguration, der ein DSC-Knoten zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9229b-103">Modifies the node configuration that a DSC node is mapped to.</span></span>

## <span data-ttu-id="9229b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9229b-104">SYNTAX</span></span>

```
Set-AzAutomationDscNode -Id <Guid> -NodeConfigurationName <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9229b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9229b-105">DESCRIPTION</span></span>
<span data-ttu-id="9229b-106">Das Cmdlet " **Satz-AzAutomationDscNode** " ändert eine APS-Knoten Konfiguration (Desired State Configuration, DSC).</span><span class="sxs-lookup"><span data-stu-id="9229b-106">The **Set-AzAutomationDscNode** cmdlet modifies an APS Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="9229b-107">Azure Automation speichert die Konfiguration des DSC-Knotens als MOF-Konfigurationsdokument (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="9229b-107">Azure Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="9229b-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9229b-108">EXAMPLES</span></span>

### <span data-ttu-id="9229b-109">Beispiel 1: Ändern der Knoten Konfigurations Zuordnung</span><span class="sxs-lookup"><span data-stu-id="9229b-109">Example 1: Modify node configuration mapping</span></span>
```
PS C:\>Set-AzAutomationDscNode -NodeConfigurationName "Contoso.NodeConfiguration01" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111c8a6067j8
```

<span data-ttu-id="9229b-110">Dieser Befehl weist die Knoten Konfiguration mit dem Namen "contoso. NodeConfiguration01" dem Knoten mit der angegebenen GUID zu.</span><span class="sxs-lookup"><span data-stu-id="9229b-110">This command assigns the node configuration named Contoso.NodeConfiguration01 to the node that has the specified GUID.</span></span>

## <span data-ttu-id="9229b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9229b-111">PARAMETERS</span></span>

### <span data-ttu-id="9229b-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9229b-112">-AutomationAccountName</span></span>
<span data-ttu-id="9229b-113">Gibt den Namen des Automatisierungs Kontos an, das den DSC-Knoten enthält, für den dieses Cmdlet die Konfiguration ändert.</span><span class="sxs-lookup"><span data-stu-id="9229b-113">Specifies the name of the Automation account that contains the DSC node for which this cmdlet modifies the configuration.</span></span>

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

### <span data-ttu-id="9229b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9229b-114">-DefaultProfile</span></span>
<span data-ttu-id="9229b-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9229b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9229b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="9229b-116">-Force</span></span>
<span data-ttu-id="9229b-117">ps_force den Befehl ausführen, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="9229b-117">ps_force the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9229b-118">-ID</span><span class="sxs-lookup"><span data-stu-id="9229b-118">-Id</span></span>
<span data-ttu-id="9229b-119">Gibt die eindeutige ID des DSC-Knotens an, für den dieses Cmdlet die Konfiguration ändert.</span><span class="sxs-lookup"><span data-stu-id="9229b-119">Specifies the unique ID of the DSC node for which this cmdlet modifies the configuration.</span></span>

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

### <span data-ttu-id="9229b-120">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="9229b-120">-NodeConfigurationName</span></span>
<span data-ttu-id="9229b-121">Gibt den Namen der Knoten Konfiguration an, der das Cmdlet den Knoten zuordnet.</span><span class="sxs-lookup"><span data-stu-id="9229b-121">Specifies the name of the node configuration to which this cmdlet maps the node.</span></span>

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

### <span data-ttu-id="9229b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9229b-122">-ResourceGroupName</span></span>
<span data-ttu-id="9229b-123">Gibt den Namen einer Ressourcengruppe an, in der mit diesem Cmdlet eine DSC-Knoten Konfiguration geändert wird.</span><span class="sxs-lookup"><span data-stu-id="9229b-123">Specifies the name of a resource group in which this cmdlet modifies a DSC node configuration.</span></span>

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

### <span data-ttu-id="9229b-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9229b-124">-Confirm</span></span>
<span data-ttu-id="9229b-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9229b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9229b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9229b-126">-WhatIf</span></span>
<span data-ttu-id="9229b-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9229b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9229b-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9229b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9229b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9229b-129">CommonParameters</span></span>
<span data-ttu-id="9229b-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9229b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9229b-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9229b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9229b-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9229b-132">INPUTS</span></span>

### <span data-ttu-id="9229b-133">System. GUID</span><span class="sxs-lookup"><span data-stu-id="9229b-133">System.Guid</span></span>

### <span data-ttu-id="9229b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9229b-134">System.String</span></span>

## <span data-ttu-id="9229b-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9229b-135">OUTPUTS</span></span>

### <span data-ttu-id="9229b-136">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="9229b-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="9229b-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="9229b-137">NOTES</span></span>

## <span data-ttu-id="9229b-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9229b-138">RELATED LINKS</span></span>

[<span data-ttu-id="9229b-139">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="9229b-139">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="9229b-140">Registrieren-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="9229b-140">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="9229b-141">Registrierung aufheben-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="9229b-141">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)



---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 60023C8D-EA37-41DA-97E6-AF89F7F9BADD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationDscNode.md
ms.openlocfilehash: 663573e7f4e111880c5ed0014dcad18480f665ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662596"
---
# <span data-ttu-id="5bb79-101">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="5bb79-101">Set-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="5bb79-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5bb79-102">SYNOPSIS</span></span>
<span data-ttu-id="5bb79-103">Ändert die Knoten Konfiguration, der ein DSC-Knoten zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5bb79-103">Modifies the node configuration that a DSC node is mapped to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bb79-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5bb79-104">SYNTAX</span></span>

```
Set-AzureRmAutomationDscNode -Id <Guid> -NodeConfigurationName <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5bb79-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5bb79-105">DESCRIPTION</span></span>
<span data-ttu-id="5bb79-106">Das Cmdlet " **Satz-AzureRmAutomationDscNode** " ändert eine APS-Knoten Konfiguration (Desired State Configuration, DSC).</span><span class="sxs-lookup"><span data-stu-id="5bb79-106">The **Set-AzureRmAutomationDscNode** cmdlet modifies an APS Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="5bb79-107">Azure Automation speichert die Konfiguration des DSC-Knotens als MOF-Konfigurationsdokument (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="5bb79-107">Azure Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="5bb79-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5bb79-108">EXAMPLES</span></span>

### <span data-ttu-id="5bb79-109">Beispiel 1: Ändern der Knoten Konfigurations Zuordnung</span><span class="sxs-lookup"><span data-stu-id="5bb79-109">Example 1: Modify node configuration mapping</span></span>
```
PS C:\>Set-AzureRmAutomationDscNode -NodeConfigurationName "Contoso.NodeConfiguration01" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111c8a6067j8
```

<span data-ttu-id="5bb79-110">Dieser Befehl weist die Knoten Konfiguration mit dem Namen "contoso. NodeConfiguration01" dem Knoten mit der angegebenen GUID zu.</span><span class="sxs-lookup"><span data-stu-id="5bb79-110">This command assigns the node configuration named Contoso.NodeConfiguration01 to the node that has the specified GUID.</span></span>

## <span data-ttu-id="5bb79-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="5bb79-111">PARAMETERS</span></span>

### <span data-ttu-id="5bb79-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5bb79-112">-AutomationAccountName</span></span>
<span data-ttu-id="5bb79-113">Gibt den Namen des Automatisierungs Kontos an, das den DSC-Knoten enthält, für den dieses Cmdlet die Konfiguration ändert.</span><span class="sxs-lookup"><span data-stu-id="5bb79-113">Specifies the name of the Automation account that contains the DSC node for which this cmdlet modifies the configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bb79-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bb79-114">-DefaultProfile</span></span>
<span data-ttu-id="5bb79-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5bb79-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb79-116">-Force</span><span class="sxs-lookup"><span data-stu-id="5bb79-116">-Force</span></span>
<span data-ttu-id="5bb79-117">ps_force den Befehl ausführen, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="5bb79-117">ps_force the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb79-118">-ID</span><span class="sxs-lookup"><span data-stu-id="5bb79-118">-Id</span></span>
<span data-ttu-id="5bb79-119">Gibt die eindeutige ID des DSC-Knotens an, für den dieses Cmdlet die Konfiguration ändert.</span><span class="sxs-lookup"><span data-stu-id="5bb79-119">Specifies the unique ID of the DSC node for which this cmdlet modifies the configuration.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bb79-120">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="5bb79-120">-NodeConfigurationName</span></span>
<span data-ttu-id="5bb79-121">Gibt den Namen der Knoten Konfiguration an, der das Cmdlet den Knoten zuordnet.</span><span class="sxs-lookup"><span data-stu-id="5bb79-121">Specifies the name of the node configuration to which this cmdlet maps the node.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bb79-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bb79-122">-ResourceGroupName</span></span>
<span data-ttu-id="5bb79-123">Gibt den Namen einer Ressourcengruppe an, in der mit diesem Cmdlet eine DSC-Knoten Konfiguration geändert wird.</span><span class="sxs-lookup"><span data-stu-id="5bb79-123">Specifies the name of a resource group in which this cmdlet modifies a DSC node configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bb79-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5bb79-124">-Confirm</span></span>
<span data-ttu-id="5bb79-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5bb79-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb79-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bb79-126">-WhatIf</span></span>
<span data-ttu-id="5bb79-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5bb79-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bb79-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5bb79-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb79-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bb79-129">CommonParameters</span></span>
<span data-ttu-id="5bb79-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bb79-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bb79-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bb79-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bb79-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5bb79-132">INPUTS</span></span>

### <span data-ttu-id="5bb79-133">Keine</span><span class="sxs-lookup"><span data-stu-id="5bb79-133">None</span></span>
<span data-ttu-id="5bb79-134">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="5bb79-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5bb79-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5bb79-135">OUTPUTS</span></span>

### <span data-ttu-id="5bb79-136">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="5bb79-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="5bb79-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="5bb79-137">NOTES</span></span>

## <span data-ttu-id="5bb79-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5bb79-138">RELATED LINKS</span></span>

[<span data-ttu-id="5bb79-139">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="5bb79-139">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="5bb79-140">Registrieren-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="5bb79-140">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="5bb79-141">Registrierung aufheben-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="5bb79-141">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)



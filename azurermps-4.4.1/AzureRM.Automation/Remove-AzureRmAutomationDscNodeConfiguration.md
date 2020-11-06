---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6C6C7142-31CD-4245-BC55-CB7916EA12E0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: 56ceba33845061af4e0ccdf3247bab16e079e90c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497937"
---
# <span data-ttu-id="3bdc0-101">Remove-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="3bdc0-101">Remove-AzureRmAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="3bdc0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3bdc0-102">SYNOPSIS</span></span>
<span data-ttu-id="3bdc0-103">Entfernt Metadaten aus DSC-Knoten Konfigurationen in der Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-103">Removes metadata from DSC node configurations in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3bdc0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3bdc0-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationDscNodeConfiguration [-Name] <String> [-Force] [-IgnoreNodeMappings]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bdc0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3bdc0-105">DESCRIPTION</span></span>
<span data-ttu-id="3bdc0-106">Das Cmdlet **Remove-AzureRmAutomationDscNodeConfiguration** entfernt Metadaten aus APS-Knoten Konfigurationen (Desired State Configuration, DSC) in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-106">The **Remove-AzureRmAutomationDscNodeConfiguration** cmdlet removes metadata from APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="3bdc0-107">Automatisierung speichert die Konfiguration des DSC-Knotens als MOF-Konfigurationsdokument (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="3bdc0-107">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="3bdc0-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3bdc0-108">EXAMPLES</span></span>

## <span data-ttu-id="3bdc0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3bdc0-109">PARAMETERS</span></span>

### <span data-ttu-id="3bdc0-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3bdc0-110">-AutomationAccountName</span></span>
<span data-ttu-id="3bdc0-111">Gibt den Namen eines Automatisierungs Kontos an, das die DSC-Knoten Konfigurationen enthält, für die dieses Cmdlet Metadaten entfernt.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-111">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet removes metadata.</span></span>

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

### <span data-ttu-id="3bdc0-112">-Force</span><span class="sxs-lookup"><span data-stu-id="3bdc0-112">-Force</span></span>
<span data-ttu-id="3bdc0-113">ps_force</span><span class="sxs-lookup"><span data-stu-id="3bdc0-113">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bdc0-114">-IgnoreNodeMappings</span><span class="sxs-lookup"><span data-stu-id="3bdc0-114">-IgnoreNodeMappings</span></span>
<span data-ttu-id="3bdc0-115">Gibt an, dass dieses Cmdlet Knoten Zuordnungen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-115">Indicates that this cmdlet ignores node mappings.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bdc0-116">-Name</span><span class="sxs-lookup"><span data-stu-id="3bdc0-116">-Name</span></span>
<span data-ttu-id="3bdc0-117">Gibt den Namen der DSC-Knoten Konfiguration an, für die dieses Cmdlet Metadaten entfernt.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-117">Specifies the name of the DSC node configuration for which this cmdlet removes metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bdc0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bdc0-118">-ResourceGroupName</span></span>
<span data-ttu-id="3bdc0-119">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-119">Specifies the name of a resource group.</span></span>
<span data-ttu-id="3bdc0-120">Dieses Cmdlet entfernt Metadaten für DSC-Knoten Konfigurationen in der Ressourcengruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-120">This cmdlet removes metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3bdc0-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3bdc0-121">-Confirm</span></span>
<span data-ttu-id="3bdc0-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bdc0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bdc0-123">-WhatIf</span></span>
<span data-ttu-id="3bdc0-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bdc0-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bdc0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bdc0-126">-DefaultProfile</span></span>
<span data-ttu-id="3bdc0-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3bdc0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bdc0-128">CommonParameters</span></span>
<span data-ttu-id="3bdc0-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bdc0-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bdc0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bdc0-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3bdc0-131">INPUTS</span></span>

## <span data-ttu-id="3bdc0-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3bdc0-132">OUTPUTS</span></span>

## <span data-ttu-id="3bdc0-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="3bdc0-133">NOTES</span></span>

## <span data-ttu-id="3bdc0-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3bdc0-134">RELATED LINKS</span></span>

[<span data-ttu-id="3bdc0-135">Get-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="3bdc0-135">Get-AzureRmAutomationDscNodeConfiguration</span></span>](./Get-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="3bdc0-136">Importieren-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="3bdc0-136">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="3bdc0-137">Azure Automation-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="3bdc0-137">Azure Automation Cmdlets</span></span>](./AzureRM.Automation.md)



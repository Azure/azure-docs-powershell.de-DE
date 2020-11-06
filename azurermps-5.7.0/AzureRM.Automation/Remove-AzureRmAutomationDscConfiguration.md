---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6389EE2A-12B5-46A1-A2B9-4B3CF5A55A30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: c328dcbf912b5b907f0e27c902bc7eb3dc31a44e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478777"
---
# <span data-ttu-id="5d556-101">Remove-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d556-101">Remove-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="5d556-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5d556-102">SYNOPSIS</span></span>
<span data-ttu-id="5d556-103">Entfernt DSC-Konfigurationen aus der Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="5d556-103">Removes DSC configurations from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d556-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d556-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationDscConfiguration [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5d556-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d556-105">DESCRIPTION</span></span>
<span data-ttu-id="5d556-106">Das Cmdlet **Remove-AzureRmAutomationDscConfiguration** entfernt APS-Konfigurationen (Desired State Configuration, DSC) aus Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="5d556-106">The **Remove-AzureRmAutomationDscConfiguration** cmdlet removes APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="5d556-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5d556-107">EXAMPLES</span></span>

## <span data-ttu-id="5d556-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d556-108">PARAMETERS</span></span>

### <span data-ttu-id="5d556-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5d556-109">-AutomationAccountName</span></span>
<span data-ttu-id="5d556-110">Gibt den Namen des Automatisierungs Kontos an, das DSC-Konfigurationen enthält, die von diesem Cmdlet entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="5d556-110">Specifies the name of the Automation account that contains DSC configurations that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5d556-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d556-111">-DefaultProfile</span></span>
<span data-ttu-id="5d556-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5d556-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d556-113">-Force</span><span class="sxs-lookup"><span data-stu-id="5d556-113">-Force</span></span>
<span data-ttu-id="5d556-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="5d556-114">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d556-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5d556-115">-Name</span></span>
<span data-ttu-id="5d556-116">Gibt den Namen der DSC-Konfiguration an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="5d556-116">Specifies the name of the DSC configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d556-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d556-117">-ResourceGroupName</span></span>
<span data-ttu-id="5d556-118">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet DSC-Konfigurationen erhält.</span><span class="sxs-lookup"><span data-stu-id="5d556-118">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="5d556-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5d556-119">-Confirm</span></span>
<span data-ttu-id="5d556-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5d556-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d556-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d556-121">-WhatIf</span></span>
<span data-ttu-id="5d556-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5d556-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d556-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d556-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d556-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d556-124">CommonParameters</span></span>
<span data-ttu-id="5d556-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d556-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d556-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d556-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d556-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5d556-127">INPUTS</span></span>

### <span data-ttu-id="5d556-128">Keine</span><span class="sxs-lookup"><span data-stu-id="5d556-128">None</span></span>
<span data-ttu-id="5d556-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="5d556-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5d556-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5d556-130">OUTPUTS</span></span>

## <span data-ttu-id="5d556-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="5d556-131">NOTES</span></span>

## <span data-ttu-id="5d556-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5d556-132">RELATED LINKS</span></span>

[<span data-ttu-id="5d556-133">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d556-133">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="5d556-134">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d556-134">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="5d556-135">Importieren-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d556-135">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)



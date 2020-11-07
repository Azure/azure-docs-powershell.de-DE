---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6389EE2A-12B5-46A1-A2B9-4B3CF5A55A30
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscConfiguration.md
ms.openlocfilehash: 1a556a92d59830a4be331c8415fde0c85ddba539
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661738"
---
# <span data-ttu-id="c85dd-101">Remove-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c85dd-101">Remove-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="c85dd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c85dd-102">SYNOPSIS</span></span>
<span data-ttu-id="c85dd-103">Entfernt DSC-Konfigurationen aus der Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="c85dd-103">Removes DSC configurations from Automation.</span></span>

## <span data-ttu-id="c85dd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c85dd-104">SYNTAX</span></span>

```
Remove-AzAutomationDscConfiguration [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c85dd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c85dd-105">DESCRIPTION</span></span>
<span data-ttu-id="c85dd-106">Das Cmdlet **Remove-AzAutomationDscConfiguration** entfernt APS-Konfigurationen (Desired State Configuration, DSC) aus Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="c85dd-106">The **Remove-AzAutomationDscConfiguration** cmdlet removes APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="c85dd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c85dd-107">EXAMPLES</span></span>

## <span data-ttu-id="c85dd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c85dd-108">PARAMETERS</span></span>

### <span data-ttu-id="c85dd-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c85dd-109">-AutomationAccountName</span></span>
<span data-ttu-id="c85dd-110">Gibt den Namen des Automatisierungs Kontos an, das DSC-Konfigurationen enthält, die von diesem Cmdlet entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="c85dd-110">Specifies the name of the Automation account that contains DSC configurations that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c85dd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c85dd-111">-DefaultProfile</span></span>
<span data-ttu-id="c85dd-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c85dd-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c85dd-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c85dd-113">-Force</span></span>
<span data-ttu-id="c85dd-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="c85dd-114">ps_force</span></span>

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

### <span data-ttu-id="c85dd-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c85dd-115">-Name</span></span>
<span data-ttu-id="c85dd-116">Gibt den Namen der DSC-Konfiguration an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c85dd-116">Specifies the name of the DSC configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c85dd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c85dd-117">-ResourceGroupName</span></span>
<span data-ttu-id="c85dd-118">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet DSC-Konfigurationen erhält.</span><span class="sxs-lookup"><span data-stu-id="c85dd-118">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="c85dd-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c85dd-119">-Confirm</span></span>
<span data-ttu-id="c85dd-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c85dd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c85dd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c85dd-121">-WhatIf</span></span>
<span data-ttu-id="c85dd-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c85dd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c85dd-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c85dd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c85dd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c85dd-124">CommonParameters</span></span>
<span data-ttu-id="c85dd-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c85dd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c85dd-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c85dd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c85dd-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c85dd-127">INPUTS</span></span>

### <span data-ttu-id="c85dd-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c85dd-128">System.String</span></span>

## <span data-ttu-id="c85dd-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c85dd-129">OUTPUTS</span></span>

### <span data-ttu-id="c85dd-130">System. void</span><span class="sxs-lookup"><span data-stu-id="c85dd-130">System.Void</span></span>

## <span data-ttu-id="c85dd-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="c85dd-131">NOTES</span></span>

## <span data-ttu-id="c85dd-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c85dd-132">RELATED LINKS</span></span>

[<span data-ttu-id="c85dd-133">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c85dd-133">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="c85dd-134">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c85dd-134">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

[<span data-ttu-id="c85dd-135">Importieren-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c85dd-135">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)



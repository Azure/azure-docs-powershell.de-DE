---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6389EE2A-12B5-46A1-A2B9-4B3CF5A55A30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: e5d7f6c75624fcfb15fa08718acc24e02336cb5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662531"
---
# <span data-ttu-id="40230-101">Remove-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="40230-101">Remove-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="40230-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="40230-102">SYNOPSIS</span></span>
<span data-ttu-id="40230-103">Entfernt DSC-Konfigurationen aus der Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="40230-103">Removes DSC configurations from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40230-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="40230-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationDscConfiguration [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="40230-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="40230-105">DESCRIPTION</span></span>
<span data-ttu-id="40230-106">Das Cmdlet **Remove-AzureRmAutomationDscConfiguration** entfernt APS-Konfigurationen (Desired State Configuration, DSC) aus Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="40230-106">The **Remove-AzureRmAutomationDscConfiguration** cmdlet removes APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="40230-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="40230-107">EXAMPLES</span></span>

## <span data-ttu-id="40230-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="40230-108">PARAMETERS</span></span>

### <span data-ttu-id="40230-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="40230-109">-AutomationAccountName</span></span>
<span data-ttu-id="40230-110">Gibt den Namen des Automatisierungs Kontos an, das DSC-Konfigurationen enthält, die von diesem Cmdlet entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="40230-110">Specifies the name of the Automation account that contains DSC configurations that this cmdlet removes.</span></span>

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

### <span data-ttu-id="40230-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40230-111">-DefaultProfile</span></span>
<span data-ttu-id="40230-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="40230-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40230-113">-Force</span><span class="sxs-lookup"><span data-stu-id="40230-113">-Force</span></span>
<span data-ttu-id="40230-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="40230-114">ps_force</span></span>

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

### <span data-ttu-id="40230-115">-Name</span><span class="sxs-lookup"><span data-stu-id="40230-115">-Name</span></span>
<span data-ttu-id="40230-116">Gibt den Namen der DSC-Konfiguration an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="40230-116">Specifies the name of the DSC configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="40230-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40230-117">-ResourceGroupName</span></span>
<span data-ttu-id="40230-118">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet DSC-Konfigurationen erhält.</span><span class="sxs-lookup"><span data-stu-id="40230-118">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="40230-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="40230-119">-Confirm</span></span>
<span data-ttu-id="40230-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="40230-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40230-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40230-121">-WhatIf</span></span>
<span data-ttu-id="40230-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="40230-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40230-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="40230-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40230-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40230-124">CommonParameters</span></span>
<span data-ttu-id="40230-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40230-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40230-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40230-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40230-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="40230-127">INPUTS</span></span>

### <span data-ttu-id="40230-128">System. String</span><span class="sxs-lookup"><span data-stu-id="40230-128">System.String</span></span>

## <span data-ttu-id="40230-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="40230-129">OUTPUTS</span></span>

### <span data-ttu-id="40230-130">System. void</span><span class="sxs-lookup"><span data-stu-id="40230-130">System.Void</span></span>

## <span data-ttu-id="40230-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="40230-131">NOTES</span></span>

## <span data-ttu-id="40230-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="40230-132">RELATED LINKS</span></span>

[<span data-ttu-id="40230-133">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="40230-133">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="40230-134">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="40230-134">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="40230-135">Importieren-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="40230-135">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)



---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6389EE2A-12B5-46A1-A2B9-4B3CF5A55A30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 2cd60a70b057689cf7edf154df28253b86e110a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497938"
---
# <span data-ttu-id="8f09b-101">Remove-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f09b-101">Remove-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="8f09b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8f09b-102">SYNOPSIS</span></span>
<span data-ttu-id="8f09b-103">Entfernt DSC-Konfigurationen aus der Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="8f09b-103">Removes DSC configurations from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f09b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f09b-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationDscConfiguration [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8f09b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8f09b-105">DESCRIPTION</span></span>
<span data-ttu-id="8f09b-106">Das Cmdlet **Remove-AzureRmAutomationDscConfiguration** entfernt APS-Konfigurationen (Desired State Configuration, DSC) aus Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="8f09b-106">The **Remove-AzureRmAutomationDscConfiguration** cmdlet removes APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="8f09b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8f09b-107">EXAMPLES</span></span>

## <span data-ttu-id="8f09b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f09b-108">PARAMETERS</span></span>

### <span data-ttu-id="8f09b-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8f09b-109">-AutomationAccountName</span></span>
<span data-ttu-id="8f09b-110">Gibt den Namen des Automatisierungs Kontos an, das DSC-Konfigurationen enthält, die von diesem Cmdlet entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="8f09b-110">Specifies the name of the Automation account that contains DSC configurations that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8f09b-111">-Force</span><span class="sxs-lookup"><span data-stu-id="8f09b-111">-Force</span></span>
<span data-ttu-id="8f09b-112">ps_force</span><span class="sxs-lookup"><span data-stu-id="8f09b-112">ps_force</span></span>

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

### <span data-ttu-id="8f09b-113">-Name</span><span class="sxs-lookup"><span data-stu-id="8f09b-113">-Name</span></span>
<span data-ttu-id="8f09b-114">Gibt den Namen der DSC-Konfiguration an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="8f09b-114">Specifies the name of the DSC configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8f09b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f09b-115">-ResourceGroupName</span></span>
<span data-ttu-id="8f09b-116">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet DSC-Konfigurationen erhält.</span><span class="sxs-lookup"><span data-stu-id="8f09b-116">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="8f09b-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8f09b-117">-Confirm</span></span>
<span data-ttu-id="8f09b-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8f09b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f09b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f09b-119">-WhatIf</span></span>
<span data-ttu-id="8f09b-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8f09b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f09b-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8f09b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f09b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f09b-122">-DefaultProfile</span></span>
<span data-ttu-id="8f09b-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8f09b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f09b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f09b-124">CommonParameters</span></span>
<span data-ttu-id="8f09b-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f09b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f09b-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f09b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f09b-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8f09b-127">INPUTS</span></span>

## <span data-ttu-id="8f09b-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8f09b-128">OUTPUTS</span></span>

## <span data-ttu-id="8f09b-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="8f09b-129">NOTES</span></span>

## <span data-ttu-id="8f09b-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8f09b-130">RELATED LINKS</span></span>

[<span data-ttu-id="8f09b-131">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f09b-131">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="8f09b-132">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f09b-132">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="8f09b-133">Importieren-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f09b-133">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)



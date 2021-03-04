---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: https://docs.microsoft.com/powershell/module/az.automation/export-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
ms.openlocfilehash: c27f878d2dbb0e52a16216a2158c737bc523c932
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922131"
---
# <span data-ttu-id="8e4d3-101">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e4d3-101">Export-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="8e4d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e4d3-102">SYNOPSIS</span></span>
<span data-ttu-id="8e4d3-103">Exportiert eine DSC-Konfiguration aus der Automatisierung in eine lokale Datei.</span><span class="sxs-lookup"><span data-stu-id="8e4d3-103">Exports a DSC configuration from Automation to a local file.</span></span>

## <span data-ttu-id="8e4d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e4d3-104">SYNTAX</span></span>

```
Export-AzAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e4d3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e4d3-105">DESCRIPTION</span></span>
<span data-ttu-id="8e4d3-106">Das **Cmdlet Export-AzAutomationDscConfiguration** exportiert eine APS Desired State Configuration (DSC)-Konfiguration aus Azure Automation in eine lokale Datei.</span><span class="sxs-lookup"><span data-stu-id="8e4d3-106">The **Export-AzAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="8e4d3-107">Die exportierte Datei verfügt über eine PS1-Dateinamenerweiterung.</span><span class="sxs-lookup"><span data-stu-id="8e4d3-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="8e4d3-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8e4d3-108">EXAMPLES</span></span>

### <span data-ttu-id="8e4d3-109">Beispiel 1: Exportieren der veröffentlichten Version einer DSC-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="8e4d3-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="8e4d3-110">Mit diesem Befehl wird die veröffentlichte Version einer DSC-Konfiguration in Automation in den angegebenen Ordner exportiert, bei dem es sich um den Desktop handelt.</span><span class="sxs-lookup"><span data-stu-id="8e4d3-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="8e4d3-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8e4d3-111">PARAMETERS</span></span>

### <span data-ttu-id="8e4d3-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8e4d3-112">-AutomationAccountName</span></span>
<span data-ttu-id="8e4d3-113">Gibt den Namen des Automatisierungskontos an, das den DSC enthält, den dieses Cmdlet exportiert.</span><span class="sxs-lookup"><span data-stu-id="8e4d3-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

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

### <span data-ttu-id="8e4d3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e4d3-114">-DefaultProfile</span></span>
<span data-ttu-id="8e4d3-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="8e4d3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e4d3-116">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="8e4d3-116">-Force</span></span>
<span data-ttu-id="8e4d3-117">Gibt an, dass dieses Cmdlet eine vorhandene lokale Datei durch eine neue Datei ersetzt, die denselben Namen hat.</span><span class="sxs-lookup"><span data-stu-id="8e4d3-117">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="8e4d3-118">-Name</span><span class="sxs-lookup"><span data-stu-id="8e4d3-118">-Name</span></span>
<span data-ttu-id="8e4d3-119">Gibt den Namen der DSC-Konfiguration an, die von diesem Cmdlet exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="8e4d3-119">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e4d3-120">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="8e4d3-120">-OutputFolder</span></span>
<span data-ttu-id="8e4d3-121">Gibt den Ausgabeordner an, in dem dieses Cmdlet die DSC-Konfiguration exportiert.</span><span class="sxs-lookup"><span data-stu-id="8e4d3-121">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e4d3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e4d3-122">-ResourceGroupName</span></span>
<span data-ttu-id="8e4d3-123">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet eine DSC-Konfiguration exportiert.</span><span class="sxs-lookup"><span data-stu-id="8e4d3-123">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

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

### <span data-ttu-id="8e4d3-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="8e4d3-124">-Slot</span></span>
<span data-ttu-id="8e4d3-125">Gibt an, welche Version der DSC-Konfiguration dieses Cmdlet exportiert.</span><span class="sxs-lookup"><span data-stu-id="8e4d3-125">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="8e4d3-126">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="8e4d3-126">Valid values are:</span></span> 
- <span data-ttu-id="8e4d3-127">Entwurf</span><span class="sxs-lookup"><span data-stu-id="8e4d3-127">Draft</span></span>
- <span data-ttu-id="8e4d3-128">Veröffentlicht Der Standardwert ist Veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="8e4d3-128">Published The default value is Published.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e4d3-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8e4d3-129">-Confirm</span></span>
<span data-ttu-id="8e4d3-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8e4d3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e4d3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e4d3-131">-WhatIf</span></span>
<span data-ttu-id="8e4d3-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8e4d3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e4d3-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8e4d3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e4d3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e4d3-134">CommonParameters</span></span>
<span data-ttu-id="8e4d3-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e4d3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e4d3-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e4d3-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e4d3-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8e4d3-137">INPUTS</span></span>

### <span data-ttu-id="8e4d3-138">System.String</span><span class="sxs-lookup"><span data-stu-id="8e4d3-138">System.String</span></span>

## <span data-ttu-id="8e4d3-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8e4d3-139">OUTPUTS</span></span>

### <span data-ttu-id="8e4d3-140">System.IO.DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="8e4d3-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="8e4d3-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8e4d3-141">NOTES</span></span>

## <span data-ttu-id="8e4d3-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8e4d3-142">RELATED LINKS</span></span>

[<span data-ttu-id="8e4d3-143">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e4d3-143">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

[<span data-ttu-id="8e4d3-144">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e4d3-144">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)



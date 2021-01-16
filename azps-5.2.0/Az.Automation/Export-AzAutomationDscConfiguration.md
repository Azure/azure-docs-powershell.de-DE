---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
ms.openlocfilehash: 27fbac9c368725a25845454adf044c2ff6704f3d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292049"
---
# <span data-ttu-id="62dd1-101">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="62dd1-101">Export-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="62dd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62dd1-102">SYNOPSIS</span></span>
<span data-ttu-id="62dd1-103">Exportiert eine DSC-Konfiguration aus der Automatisierung in eine lokale Datei.</span><span class="sxs-lookup"><span data-stu-id="62dd1-103">Exports a DSC configuration from Automation to a local file.</span></span>

## <span data-ttu-id="62dd1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="62dd1-104">SYNTAX</span></span>

```
Export-AzAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62dd1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="62dd1-105">DESCRIPTION</span></span>
<span data-ttu-id="62dd1-106">Das **Cmdlet "Export-AzAutomationDscConfiguration"** exportiert eine Konfiguration der APS Desired State Configuration (DSC) aus der Azure Automation in eine lokale Datei.</span><span class="sxs-lookup"><span data-stu-id="62dd1-106">The **Export-AzAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="62dd1-107">Die exportierte Datei hat die Dateinamenerweiterung PS1.</span><span class="sxs-lookup"><span data-stu-id="62dd1-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="62dd1-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="62dd1-108">EXAMPLES</span></span>

### <span data-ttu-id="62dd1-109">Beispiel 1: Exportieren der veröffentlichten Version einer DSC-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="62dd1-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="62dd1-110">Mit diesem Befehl wird die veröffentlichte Version einer DSC-Konfiguration in der Automatisierung in den angegebenen Ordner exportiert, bei dem es sich um den Desktop handelt.</span><span class="sxs-lookup"><span data-stu-id="62dd1-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="62dd1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62dd1-111">PARAMETERS</span></span>

### <span data-ttu-id="62dd1-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="62dd1-112">-AutomationAccountName</span></span>
<span data-ttu-id="62dd1-113">Gibt den Namen des Automatisierungskontos an, das den DSC enthält, den dieses Cmdlet exportiert.</span><span class="sxs-lookup"><span data-stu-id="62dd1-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

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

### <span data-ttu-id="62dd1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62dd1-114">-DefaultProfile</span></span>
<span data-ttu-id="62dd1-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="62dd1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62dd1-116">-Force</span><span class="sxs-lookup"><span data-stu-id="62dd1-116">-Force</span></span>
<span data-ttu-id="62dd1-117">Gibt an, dass dieses Cmdlet eine vorhandene lokale Datei durch eine neue Datei mit demselben Namen ersetzt.</span><span class="sxs-lookup"><span data-stu-id="62dd1-117">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="62dd1-118">-Name</span><span class="sxs-lookup"><span data-stu-id="62dd1-118">-Name</span></span>
<span data-ttu-id="62dd1-119">Gibt den Namen der DSC-Konfiguration an, die von diesem Cmdlet exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="62dd1-119">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

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

### <span data-ttu-id="62dd1-120">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="62dd1-120">-OutputFolder</span></span>
<span data-ttu-id="62dd1-121">Gibt den Ausgabeordner an, in den dieses Cmdlet die DSC-Konfiguration exportiert.</span><span class="sxs-lookup"><span data-stu-id="62dd1-121">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

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

### <span data-ttu-id="62dd1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62dd1-122">-ResourceGroupName</span></span>
<span data-ttu-id="62dd1-123">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet eine -DSC-Konfiguration exportiert.</span><span class="sxs-lookup"><span data-stu-id="62dd1-123">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

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

### <span data-ttu-id="62dd1-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="62dd1-124">-Slot</span></span>
<span data-ttu-id="62dd1-125">Gibt an, welche Version der DSC-Konfiguration, die von diesem Cmdlet exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="62dd1-125">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="62dd1-126">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="62dd1-126">Valid values are:</span></span> 
- <span data-ttu-id="62dd1-127">Entwurf</span><span class="sxs-lookup"><span data-stu-id="62dd1-127">Draft</span></span>
- <span data-ttu-id="62dd1-128">Veröffentlicht Der Standardwert ist "Veröffentlicht".</span><span class="sxs-lookup"><span data-stu-id="62dd1-128">Published The default value is Published.</span></span>

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

### <span data-ttu-id="62dd1-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62dd1-129">-Confirm</span></span>
<span data-ttu-id="62dd1-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="62dd1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62dd1-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="62dd1-131">-WhatIf</span></span>
<span data-ttu-id="62dd1-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="62dd1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62dd1-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="62dd1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62dd1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62dd1-134">CommonParameters</span></span>
<span data-ttu-id="62dd1-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62dd1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62dd1-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62dd1-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62dd1-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="62dd1-137">INPUTS</span></span>

### <span data-ttu-id="62dd1-138">System.String</span><span class="sxs-lookup"><span data-stu-id="62dd1-138">System.String</span></span>

## <span data-ttu-id="62dd1-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="62dd1-139">OUTPUTS</span></span>

### <span data-ttu-id="62dd1-140">System.IO.DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="62dd1-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="62dd1-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="62dd1-141">NOTES</span></span>

## <span data-ttu-id="62dd1-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="62dd1-142">RELATED LINKS</span></span>

[<span data-ttu-id="62dd1-143">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="62dd1-143">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

[<span data-ttu-id="62dd1-144">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="62dd1-144">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)



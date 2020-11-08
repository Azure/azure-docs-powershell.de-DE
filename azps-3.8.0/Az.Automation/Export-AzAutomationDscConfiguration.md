---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
ms.openlocfilehash: 27fbac9c368725a25845454adf044c2ff6704f3d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997422"
---
# <span data-ttu-id="37d52-101">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="37d52-101">Export-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="37d52-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="37d52-102">SYNOPSIS</span></span>
<span data-ttu-id="37d52-103">Exportiert eine DSC-Konfiguration aus der Automatisierung in eine lokale Datei.</span><span class="sxs-lookup"><span data-stu-id="37d52-103">Exports a DSC configuration from Automation to a local file.</span></span>

## <span data-ttu-id="37d52-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="37d52-104">SYNTAX</span></span>

```
Export-AzAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37d52-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37d52-105">DESCRIPTION</span></span>
<span data-ttu-id="37d52-106">Das Cmdlet **Export-AzAutomationDscConfiguration** exportiert eine APS-Konfiguration (Desired State Configuration, DSC) aus Azure Automation in eine lokale Datei.</span><span class="sxs-lookup"><span data-stu-id="37d52-106">The **Export-AzAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="37d52-107">Die exportierte Datei hat die Dateinamenerweiterung PS1.</span><span class="sxs-lookup"><span data-stu-id="37d52-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="37d52-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37d52-108">EXAMPLES</span></span>

### <span data-ttu-id="37d52-109">Beispiel 1: Exportieren der veröffentlichten Version einer DSC-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="37d52-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="37d52-110">Mit diesem Befehl wird die veröffentlichte Version einer DSC-Konfiguration in der Automatisierung in den angegebenen Ordner, also den Desktop, exportiert.</span><span class="sxs-lookup"><span data-stu-id="37d52-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="37d52-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="37d52-111">PARAMETERS</span></span>

### <span data-ttu-id="37d52-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="37d52-112">-AutomationAccountName</span></span>
<span data-ttu-id="37d52-113">Gibt den Namen des Automatisierungs Kontos an, das die vom Cmdlet exportierte DSC-Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="37d52-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

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

### <span data-ttu-id="37d52-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37d52-114">-DefaultProfile</span></span>
<span data-ttu-id="37d52-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="37d52-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37d52-116">-Force</span><span class="sxs-lookup"><span data-stu-id="37d52-116">-Force</span></span>
<span data-ttu-id="37d52-117">Gibt an, dass dieses Cmdlet eine vorhandene lokale Datei durch eine neue Datei ersetzt, die denselben Namen aufweist.</span><span class="sxs-lookup"><span data-stu-id="37d52-117">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="37d52-118">-Name</span><span class="sxs-lookup"><span data-stu-id="37d52-118">-Name</span></span>
<span data-ttu-id="37d52-119">Gibt den Namen der DSC-Konfiguration an, die dieses Cmdlet exportiert.</span><span class="sxs-lookup"><span data-stu-id="37d52-119">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

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

### <span data-ttu-id="37d52-120">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="37d52-120">-OutputFolder</span></span>
<span data-ttu-id="37d52-121">Gibt den Ausgabeordner an, in dem dieses Cmdlet die DSC-Konfiguration exportiert.</span><span class="sxs-lookup"><span data-stu-id="37d52-121">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

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

### <span data-ttu-id="37d52-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37d52-122">-ResourceGroupName</span></span>
<span data-ttu-id="37d52-123">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet eine DSC-Konfiguration exportiert.</span><span class="sxs-lookup"><span data-stu-id="37d52-123">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

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

### <span data-ttu-id="37d52-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="37d52-124">-Slot</span></span>
<span data-ttu-id="37d52-125">Gibt an, welche Version der DSC-Konfiguration vom Cmdlet exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="37d52-125">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="37d52-126">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="37d52-126">Valid values are:</span></span> 
- <span data-ttu-id="37d52-127">Entwurf</span><span class="sxs-lookup"><span data-stu-id="37d52-127">Draft</span></span>
- <span data-ttu-id="37d52-128">Veröffentlicht der Standardwert wird veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="37d52-128">Published The default value is Published.</span></span>

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

### <span data-ttu-id="37d52-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="37d52-129">-Confirm</span></span>
<span data-ttu-id="37d52-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="37d52-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37d52-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37d52-131">-WhatIf</span></span>
<span data-ttu-id="37d52-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37d52-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37d52-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37d52-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37d52-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37d52-134">CommonParameters</span></span>
<span data-ttu-id="37d52-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37d52-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37d52-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37d52-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37d52-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="37d52-137">INPUTS</span></span>

### <span data-ttu-id="37d52-138">System. String</span><span class="sxs-lookup"><span data-stu-id="37d52-138">System.String</span></span>

## <span data-ttu-id="37d52-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="37d52-139">OUTPUTS</span></span>

### <span data-ttu-id="37d52-140">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="37d52-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="37d52-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="37d52-141">NOTES</span></span>

## <span data-ttu-id="37d52-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="37d52-142">RELATED LINKS</span></span>

[<span data-ttu-id="37d52-143">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="37d52-143">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

[<span data-ttu-id="37d52-144">Importieren-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="37d52-144">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CC9D74BB-DFB2-41F3-B5CF-B265C549EC33
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/import-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 3036b02d280542ffa4c8eea85dafed2da8eb5e28
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471324"
---
# <span data-ttu-id="2fd66-101">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fd66-101">Import-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="2fd66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fd66-102">SYNOPSIS</span></span>
<span data-ttu-id="2fd66-103">Importiert ein MOF-Dokument als DSC-Knotenkonfiguration in der Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="2fd66-103">Imports a MOF document as a DSC node configuration in Automation.</span></span>

## <span data-ttu-id="2fd66-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2fd66-104">SYNTAX</span></span>

```
Import-AzAutomationDscNodeConfiguration -Path <String> -ConfigurationName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fd66-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2fd66-105">DESCRIPTION</span></span>
<span data-ttu-id="2fd66-106">Das **Cmdlet "Import-AzAutomationDscConfiguration"** importiert ein Konfigurationsdokument für verwaltetes Objektformat (Managed Object Format, MOF) als DSC (Desired State Configuration)-Knotenkonfiguration in die Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="2fd66-106">The **Import-AzAutomationDscConfiguration** cmdlet imports a Managed Object Format (MOF) configuration document into Azure Automation as a Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="2fd66-107">Geben Sie den Pfad einer MOF-Datei an.</span><span class="sxs-lookup"><span data-stu-id="2fd66-107">Specify the path of a .mof file.</span></span>

## <span data-ttu-id="2fd66-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2fd66-108">EXAMPLES</span></span>

### <span data-ttu-id="2fd66-109">Beispiel 1: Importieren einer Konfiguration eines DSC-Knotens in die Automatisierung</span><span class="sxs-lookup"><span data-stu-id="2fd66-109">Example 1: Import a DSC node configuration into Automation</span></span>
```
PS C:\>Import-AzAutomationDscNodeConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -Force
```

<span data-ttu-id="2fd66-110">Mit diesem Befehl wird eine KONFIGURATION des DSC-Knotens aus der Datei "webserver.mof" in das Automatisierungskonto namens "Contoso17" unter der KONFIGURATION "ContosoConfiguration" importiert.</span><span class="sxs-lookup"><span data-stu-id="2fd66-110">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="2fd66-111">Der Befehl gibt den Parameter *"Force"* an.</span><span class="sxs-lookup"><span data-stu-id="2fd66-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="2fd66-112">Wenn es eine vorhandene Konfiguration des DSC-Knotens "ContosoConfiguration.webserver" gibt, wird sie durch diesen Befehl ersetzt.</span><span class="sxs-lookup"><span data-stu-id="2fd66-112">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command replaces it.</span></span>

### <span data-ttu-id="2fd66-113">Beispiel 2: Importieren sie eine DSC-Knotenkonfiguration in die Automatisierung, und erstellen Sie eine neue Buildversion, und überschreiben Sie nicht die vorhandene NodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2fd66-113">Example 2: Import a DSC node configuration into Automation and create a new build version and not overwrite existing NodeConfiguration.</span></span>
```
PS C:\>Import-AzAutomationDscNodeConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="2fd66-114">Mit diesem Befehl wird eine KONFIGURATION des DSC-Knotens aus der Datei "webserver.mof" in das Automatisierungskonto namens "Contoso17" unter der KONFIGURATION "ContosoConfiguration" importiert.</span><span class="sxs-lookup"><span data-stu-id="2fd66-114">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="2fd66-115">Der Befehl gibt den Parameter *"Force"* an.</span><span class="sxs-lookup"><span data-stu-id="2fd66-115">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="2fd66-116">Wenn eine #A0 mit dem Namen "ContosoConfiguration.webserver" vorhanden ist, wird mit diesem Befehl eine neue Buildversion mit dem Namen "ContosoConfiguration[2].webserver" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2fd66-116">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command adds a new build version with the name ContosoConfiguration[2].webserver.</span></span>

## <span data-ttu-id="2fd66-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2fd66-117">PARAMETERS</span></span>

### <span data-ttu-id="2fd66-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2fd66-118">-AutomationAccountName</span></span>
<span data-ttu-id="2fd66-119">Gibt den Namen des Automatisierungskontos an, in das dieses Cmdlet eine DSC-Knotenkonfiguration importiert.</span><span class="sxs-lookup"><span data-stu-id="2fd66-119">Specifies the name of the Automation account into which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="2fd66-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="2fd66-120">-ConfigurationName</span></span>
<span data-ttu-id="2fd66-121">Gibt den Namen einer DSC-Konfiguration in der Automatisierung an, die als Namespace und Container für die zu importierende Knotenkonfiguration verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2fd66-121">Specifies the name of a DSC configuration in Automation to use as the namespace and container for the node configuration to import.</span></span>

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

### <span data-ttu-id="2fd66-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fd66-122">-DefaultProfile</span></span>
<span data-ttu-id="2fd66-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="2fd66-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2fd66-124">-Force</span><span class="sxs-lookup"><span data-stu-id="2fd66-124">-Force</span></span>
<span data-ttu-id="2fd66-125">Gibt an, dass dieses Cmdlet eine vorhandene Konfiguration des DSC-Knotens in der Automatisierung ersetzt.</span><span class="sxs-lookup"><span data-stu-id="2fd66-125">Indicates that this cmdlet replaces an existing DSC node configuration in Automation.</span></span>

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

### <span data-ttu-id="2fd66-126">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="2fd66-126">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="2fd66-127">Erstellt eine neue Buildversion der Knotenkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="2fd66-127">Creates a new Node Configuration build version.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fd66-128">-Path</span><span class="sxs-lookup"><span data-stu-id="2fd66-128">-Path</span></span>
<span data-ttu-id="2fd66-129">Gibt den Pfad des MOF-Konfigurationsdokuments an, das von diesem Cmdlet importiert wird.</span><span class="sxs-lookup"><span data-stu-id="2fd66-129">Specifies the path of the MOF configuration document that this cmdlet imports.</span></span>

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

### <span data-ttu-id="2fd66-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fd66-130">-ResourceGroupName</span></span>
<span data-ttu-id="2fd66-131">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet eine DSC-Knotenkonfiguration importiert.</span><span class="sxs-lookup"><span data-stu-id="2fd66-131">Specifies the name of a resource group for which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="2fd66-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2fd66-132">-Confirm</span></span>
<span data-ttu-id="2fd66-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2fd66-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fd66-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2fd66-134">-WhatIf</span></span>
<span data-ttu-id="2fd66-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2fd66-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fd66-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2fd66-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fd66-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fd66-137">CommonParameters</span></span>
<span data-ttu-id="2fd66-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fd66-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fd66-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fd66-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fd66-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2fd66-140">INPUTS</span></span>

### <span data-ttu-id="2fd66-141">System.String</span><span class="sxs-lookup"><span data-stu-id="2fd66-141">System.String</span></span>

## <span data-ttu-id="2fd66-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2fd66-142">OUTPUTS</span></span>

### <span data-ttu-id="2fd66-143">Microsoft.Azure.Commands.Automation.Model.NodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fd66-143">Microsoft.Azure.Commands.Automation.Model.NodeConfiguration</span></span>

## <span data-ttu-id="2fd66-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2fd66-144">NOTES</span></span>

## <span data-ttu-id="2fd66-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2fd66-145">RELATED LINKS</span></span>

[<span data-ttu-id="2fd66-146">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fd66-146">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="2fd66-147">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fd66-147">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)



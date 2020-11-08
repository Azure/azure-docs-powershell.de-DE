---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CC9D74BB-DFB2-41F3-B5CF-B265C549EC33
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/import-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 3036b02d280542ffa4c8eea85dafed2da8eb5e28
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005188"
---
# <span data-ttu-id="11901-101">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="11901-101">Import-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="11901-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="11901-102">SYNOPSIS</span></span>
<span data-ttu-id="11901-103">Importiert ein MOF-Dokument als DSC-Knoten Konfiguration in der Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="11901-103">Imports a MOF document as a DSC node configuration in Automation.</span></span>

## <span data-ttu-id="11901-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="11901-104">SYNTAX</span></span>

```
Import-AzAutomationDscNodeConfiguration -Path <String> -ConfigurationName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11901-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11901-105">DESCRIPTION</span></span>
<span data-ttu-id="11901-106">Mit dem Cmdlet " **Import-AzAutomationDscConfiguration** " wird ein MOF-Konfigurationsdokument (Managed Object Format) in die Azure-Automatisierung als Konfiguration für eine gewünschte Statuskonfiguration (DSC) importiert.</span><span class="sxs-lookup"><span data-stu-id="11901-106">The **Import-AzAutomationDscConfiguration** cmdlet imports a Managed Object Format (MOF) configuration document into Azure Automation as a Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="11901-107">Geben Sie den Pfad einer MOF-Datei an.</span><span class="sxs-lookup"><span data-stu-id="11901-107">Specify the path of a .mof file.</span></span>

## <span data-ttu-id="11901-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="11901-108">EXAMPLES</span></span>

### <span data-ttu-id="11901-109">Beispiel 1: Importieren einer DSC-Knoten Konfiguration in die Automatisierung</span><span class="sxs-lookup"><span data-stu-id="11901-109">Example 1: Import a DSC node configuration into Automation</span></span>
```
PS C:\>Import-AzAutomationDscNodeConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -Force
```

<span data-ttu-id="11901-110">Dieser Befehl importiert eine DSC-Knoten Konfiguration aus der Datei "Webserver. mof" in das Automatisierungs Konto mit dem Namen Contoso17 unter dem DSC-Konfigurations ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="11901-110">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="11901-111">Der Befehl gibt den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="11901-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="11901-112">Wenn eine vorhandene DSC-Knoten Konfiguration mit dem Namen ContosoConfiguration. Webserver vorhanden ist, wird Sie durch diesen Befehl ersetzt.</span><span class="sxs-lookup"><span data-stu-id="11901-112">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command replaces it.</span></span>

### <span data-ttu-id="11901-113">Beispiel 2: Importieren Sie eine DSC-Knoten Konfiguration in die Automatisierung, und erstellen Sie eine neue Buildversion, und überschreiben Sie keine vorhandenen NodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="11901-113">Example 2: Import a DSC node configuration into Automation and create a new build version and not overwrite existing NodeConfiguration.</span></span>
```
PS C:\>Import-AzAutomationDscNodeConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="11901-114">Dieser Befehl importiert eine DSC-Knoten Konfiguration aus der Datei "Webserver. mof" in das Automatisierungs Konto mit dem Namen Contoso17 unter dem DSC-Konfigurations ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="11901-114">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="11901-115">Der Befehl gibt den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="11901-115">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="11901-116">Wenn eine vorhandene DSC-Knoten Konfiguration mit dem Namen ContosoConfiguration. Webserver vorhanden ist, wird mit diesem Befehl eine neue Buildversion mit dem Namen ContosoConfiguration [2]. Webserver hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="11901-116">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command adds a new build version with the name ContosoConfiguration[2].webserver.</span></span>

## <span data-ttu-id="11901-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="11901-117">PARAMETERS</span></span>

### <span data-ttu-id="11901-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="11901-118">-AutomationAccountName</span></span>
<span data-ttu-id="11901-119">Gibt den Namen des Automatisierungs Kontos an, in das dieses Cmdlet eine DSC-Knoten Konfiguration importiert.</span><span class="sxs-lookup"><span data-stu-id="11901-119">Specifies the name of the Automation account into which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="11901-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="11901-120">-ConfigurationName</span></span>
<span data-ttu-id="11901-121">Gibt den Namen einer DSC-Konfiguration in Automatisierung an, die als Namespace und Container für die zu importierende Knoten Konfiguration verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="11901-121">Specifies the name of a DSC configuration in Automation to use as the namespace and container for the node configuration to import.</span></span>

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

### <span data-ttu-id="11901-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11901-122">-DefaultProfile</span></span>
<span data-ttu-id="11901-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="11901-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11901-124">-Force</span><span class="sxs-lookup"><span data-stu-id="11901-124">-Force</span></span>
<span data-ttu-id="11901-125">Gibt an, dass dieses Cmdlet eine vorhandene DSC-Knoten Konfiguration in der Automatisierung ersetzt.</span><span class="sxs-lookup"><span data-stu-id="11901-125">Indicates that this cmdlet replaces an existing DSC node configuration in Automation.</span></span>

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

### <span data-ttu-id="11901-126">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="11901-126">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="11901-127">Erstellt eine neue Buildversion für die Knoten Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="11901-127">Creates a new Node Configuration build version.</span></span>

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

### <span data-ttu-id="11901-128">-Path</span><span class="sxs-lookup"><span data-stu-id="11901-128">-Path</span></span>
<span data-ttu-id="11901-129">Gibt den Pfad des MOF-Konfigurationsdokuments an, das von diesem Cmdlet importiert wird.</span><span class="sxs-lookup"><span data-stu-id="11901-129">Specifies the path of the MOF configuration document that this cmdlet imports.</span></span>

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

### <span data-ttu-id="11901-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11901-130">-ResourceGroupName</span></span>
<span data-ttu-id="11901-131">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet eine DSC-Knoten Konfiguration importiert.</span><span class="sxs-lookup"><span data-stu-id="11901-131">Specifies the name of a resource group for which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="11901-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="11901-132">-Confirm</span></span>
<span data-ttu-id="11901-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="11901-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11901-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11901-134">-WhatIf</span></span>
<span data-ttu-id="11901-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="11901-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11901-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="11901-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11901-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11901-137">CommonParameters</span></span>
<span data-ttu-id="11901-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11901-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11901-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11901-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11901-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="11901-140">INPUTS</span></span>

### <span data-ttu-id="11901-141">System. String</span><span class="sxs-lookup"><span data-stu-id="11901-141">System.String</span></span>

## <span data-ttu-id="11901-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="11901-142">OUTPUTS</span></span>

### <span data-ttu-id="11901-143">Microsoft. Azure. Commands. Automation. Model. NodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="11901-143">Microsoft.Azure.Commands.Automation.Model.NodeConfiguration</span></span>

## <span data-ttu-id="11901-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="11901-144">NOTES</span></span>

## <span data-ttu-id="11901-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="11901-145">RELATED LINKS</span></span>

[<span data-ttu-id="11901-146">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="11901-146">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="11901-147">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="11901-147">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)



---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BA508F0B-847F-4531-9D5D-A5A044A2D207
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/import-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 98e7875297e55660615607eef91c4187e8144fa1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498502"
---
# <span data-ttu-id="35215-101">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="35215-101">Import-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="35215-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="35215-102">SYNOPSIS</span></span>
<span data-ttu-id="35215-103">Importiert eine DSC-Konfiguration in die Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="35215-103">Imports a DSC configuration into Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35215-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="35215-104">SYNTAX</span></span>

```
Import-AzureRmAutomationDscConfiguration -SourcePath <String> [-Tags <IDictionary>] [-Description <String>]
 [-Published] [-Force] [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35215-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="35215-105">DESCRIPTION</span></span>
<span data-ttu-id="35215-106">Das Cmdlet " **Import-AzureRmAutomationDscConfiguration** " importiert eine APS-Konfiguration (Desired State Configuration, DSC) in die Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="35215-106">The **Import-AzureRmAutomationDscConfiguration** cmdlet imports an APS Desired State Configuration (DSC) configuration into Azure Automation.</span></span>
<span data-ttu-id="35215-107">Geben Sie den Pfad eines APS-Skripts an, das eine einzelne DSC-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="35215-107">Specify the path of an APS script that contains a single DSC configuration.</span></span>

## <span data-ttu-id="35215-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="35215-108">EXAMPLES</span></span>

### <span data-ttu-id="35215-109">Beispiel 1: Importieren einer DSC-Konfiguration in die Automatisierung</span><span class="sxs-lookup"><span data-stu-id="35215-109">Example 1: Import a DSC configuration into Automation</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17"-ResourceGroupName "ResourceGroup01" -SourcePath "C:\DSC\client.ps1" -Force
```

<span data-ttu-id="35215-110">Dieser Befehl importiert die DSC-Konfiguration in der Datei mit dem Namen client.ps1 in das Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="35215-110">This command imports the DSC configuration in the file named client.ps1 into the Automation account named Contoso17.</span></span> <span data-ttu-id="35215-111">Der Befehl gibt den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="35215-111">The command specifies the *Force* parameter.</span></span> <span data-ttu-id="35215-112">Wenn eine DSC-Konfiguration vorhanden ist, wird Sie durch diesen Befehl ersetzt.</span><span class="sxs-lookup"><span data-stu-id="35215-112">If there is an existing DSC configuration, this command replaces it.</span></span>

## <span data-ttu-id="35215-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="35215-113">PARAMETERS</span></span>

### <span data-ttu-id="35215-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="35215-114">-AutomationAccountName</span></span>
<span data-ttu-id="35215-115">Gibt den Namen des Automatisierungs Kontos an, in das dieses Cmdlet eine DSC-Konfiguration importiert.</span><span class="sxs-lookup"><span data-stu-id="35215-115">Specifies the name of the Automation account into which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="35215-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35215-116">-DefaultProfile</span></span>
<span data-ttu-id="35215-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="35215-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35215-118">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="35215-118">-Description</span></span>
<span data-ttu-id="35215-119">Gibt eine Beschreibung der Konfiguration an, die dieses Cmdlet importiert.</span><span class="sxs-lookup"><span data-stu-id="35215-119">Specifies a description of the configuration that this cmdlet imports.</span></span>

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

### <span data-ttu-id="35215-120">-Force</span><span class="sxs-lookup"><span data-stu-id="35215-120">-Force</span></span>
<span data-ttu-id="35215-121">Gibt an, dass dieses Cmdlet eine vorhandene DSC-Konfiguration in der Automatisierung ersetzt.</span><span class="sxs-lookup"><span data-stu-id="35215-121">Indicates that this cmdlet replaces an existing DSC configuration in Automation.</span></span>

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

### <span data-ttu-id="35215-122">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="35215-122">-LogVerbose</span></span>
<span data-ttu-id="35215-123">Gibt an, ob dieses Cmdlet die ausführliche Protokollierung für Kompilierungsaufträge dieser DSC-Konfiguration aktiviert oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="35215-123">Specifies whether this cmdlet turns verbose logging on or off for compilation jobs of this DSC configuration.</span></span> <span data-ttu-id="35215-124">Geben Sie einen Wert für $true an, um die ausführliche Protokollierung zu aktivieren oder $false, um Sie zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="35215-124">Specify a value of $True to turn verbose logging on or $False to turn it off.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35215-125">– Veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="35215-125">-Published</span></span>
<span data-ttu-id="35215-126">Gibt an, dass dieses Cmdlet die DSC-Konfiguration im veröffentlichten Zustand importiert.</span><span class="sxs-lookup"><span data-stu-id="35215-126">Indicates that this cmdlet imports the DSC configuration in the published state.</span></span>

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

### <span data-ttu-id="35215-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35215-127">-ResourceGroupName</span></span>
<span data-ttu-id="35215-128">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet eine DSC-Konfiguration importiert.</span><span class="sxs-lookup"><span data-stu-id="35215-128">Specifies the name of a resource group for which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="35215-129">-SourcePath</span><span class="sxs-lookup"><span data-stu-id="35215-129">-SourcePath</span></span>
<span data-ttu-id="35215-130">Gibt den Pfad des wps_2 Skripts an, das die DSC-Konfiguration enthält, die von diesem Cmdlet importiert wird.</span><span class="sxs-lookup"><span data-stu-id="35215-130">Specifies the path of the wps_2 script that contains the DSC configuration that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35215-131">-Tags</span><span class="sxs-lookup"><span data-stu-id="35215-131">-Tags</span></span>
<span data-ttu-id="35215-132">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="35215-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="35215-133">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="35215-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35215-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="35215-134">-Confirm</span></span>
<span data-ttu-id="35215-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="35215-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35215-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35215-136">-WhatIf</span></span>
<span data-ttu-id="35215-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="35215-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35215-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="35215-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35215-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35215-139">CommonParameters</span></span>
<span data-ttu-id="35215-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35215-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35215-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35215-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35215-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="35215-142">INPUTS</span></span>

### <span data-ttu-id="35215-143">System. String</span><span class="sxs-lookup"><span data-stu-id="35215-143">System.String</span></span>

### <span data-ttu-id="35215-144">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="35215-144">System.Collections.IDictionary</span></span>

### <span data-ttu-id="35215-145">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="35215-145">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="35215-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="35215-146">OUTPUTS</span></span>

### <span data-ttu-id="35215-147">Microsoft. Azure. Commands. Automation. Model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="35215-147">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="35215-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="35215-148">NOTES</span></span>

## <span data-ttu-id="35215-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="35215-149">RELATED LINKS</span></span>

[<span data-ttu-id="35215-150">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="35215-150">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="35215-151">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="35215-151">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

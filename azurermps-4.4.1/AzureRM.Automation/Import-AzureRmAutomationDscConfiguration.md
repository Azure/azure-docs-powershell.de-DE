---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BA508F0B-847F-4531-9D5D-A5A044A2D207
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 12cc605a95cb44b933c748156054135cb8395d61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497970"
---
# <span data-ttu-id="33d84-101">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="33d84-101">Import-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="33d84-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="33d84-102">SYNOPSIS</span></span>
<span data-ttu-id="33d84-103">Importiert eine DSC-Konfiguration in die Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="33d84-103">Imports a DSC configuration into Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33d84-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="33d84-104">SYNTAX</span></span>

```
Import-AzureRmAutomationDscConfiguration -SourcePath <String> [-Tags <IDictionary>] [-Description <String>]
 [-Published] [-Force] [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33d84-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="33d84-105">DESCRIPTION</span></span>
<span data-ttu-id="33d84-106">Das Cmdlet " **Import-AzureRmAutomationDscConfiguration** " importiert eine APS-Konfiguration (Desired State Configuration, DSC) in die Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="33d84-106">The **Import-AzureRmAutomationDscConfiguration** cmdlet imports an APS Desired State Configuration (DSC) configuration into Azure Automation.</span></span>
<span data-ttu-id="33d84-107">Geben Sie den Pfad eines APS-Skripts an, das eine einzelne DSC-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="33d84-107">Specify the path of an APS script that contains a single DSC configuration.</span></span>

## <span data-ttu-id="33d84-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="33d84-108">EXAMPLES</span></span>

### <span data-ttu-id="33d84-109">Beispiel 1: Importieren einer DSC-Konfiguration in die Automatisierung</span><span class="sxs-lookup"><span data-stu-id="33d84-109">Example 1: Import a DSC configuration into Automation</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17"-ResourceGroupName "ResourceGroup01" -SourcePath "C:\DSC\client.ps1" -Force
```

<span data-ttu-id="33d84-110">Dieser Befehl importiert die DSC-Konfiguration in der Datei mit dem Namen client.ps1 in das Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="33d84-110">This command imports the DSC configuration in the file named client.ps1 into the Automation account named Contoso17.</span></span> <span data-ttu-id="33d84-111">Der Befehl gibt den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="33d84-111">The command specifies the *Force* parameter.</span></span> <span data-ttu-id="33d84-112">Wenn eine DSC-Konfiguration vorhanden ist, wird Sie durch diesen Befehl ersetzt.</span><span class="sxs-lookup"><span data-stu-id="33d84-112">If there is an existing DSC configuration, this command replaces it.</span></span>

## <span data-ttu-id="33d84-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="33d84-113">PARAMETERS</span></span>

### <span data-ttu-id="33d84-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="33d84-114">-AutomationAccountName</span></span>
<span data-ttu-id="33d84-115">Gibt den Namen des Automatisierungs Kontos an, in das dieses Cmdlet eine DSC-Konfiguration importiert.</span><span class="sxs-lookup"><span data-stu-id="33d84-115">Specifies the name of the Automation account into which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="33d84-116">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="33d84-116">-Description</span></span>
<span data-ttu-id="33d84-117">Gibt eine Beschreibung der Konfiguration an, die dieses Cmdlet importiert.</span><span class="sxs-lookup"><span data-stu-id="33d84-117">Specifies a description of the configuration that this cmdlet imports.</span></span>

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

### <span data-ttu-id="33d84-118">-Force</span><span class="sxs-lookup"><span data-stu-id="33d84-118">-Force</span></span>
<span data-ttu-id="33d84-119">Gibt an, dass dieses Cmdlet eine vorhandene DSC-Konfiguration in der Automatisierung ersetzt.</span><span class="sxs-lookup"><span data-stu-id="33d84-119">Indicates that this cmdlet replaces an existing DSC configuration in Automation.</span></span>

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

### <span data-ttu-id="33d84-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="33d84-120">-LogVerbose</span></span>
<span data-ttu-id="33d84-121">Gibt an, ob dieses Cmdlet die ausführliche Protokollierung für Kompilierungsaufträge dieser DSC-Konfiguration aktiviert oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="33d84-121">Specifies whether this cmdlet turns verbose logging on or off for compilation jobs of this DSC configuration.</span></span> <span data-ttu-id="33d84-122">Geben Sie einen Wert für $true an, um die ausführliche Protokollierung zu aktivieren oder $false, um Sie zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="33d84-122">Specify a value of $True to turn verbose logging on or $False to turn it off.</span></span>

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

### <span data-ttu-id="33d84-123">– Veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="33d84-123">-Published</span></span>
<span data-ttu-id="33d84-124">Gibt an, dass dieses Cmdlet die DSC-Konfiguration im veröffentlichten Zustand importiert.</span><span class="sxs-lookup"><span data-stu-id="33d84-124">Indicates that this cmdlet imports the DSC configuration in the published state.</span></span>

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

### <span data-ttu-id="33d84-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33d84-125">-ResourceGroupName</span></span>
<span data-ttu-id="33d84-126">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet eine DSC-Konfiguration importiert.</span><span class="sxs-lookup"><span data-stu-id="33d84-126">Specifies the name of a resource group for which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="33d84-127">-SourcePath</span><span class="sxs-lookup"><span data-stu-id="33d84-127">-SourcePath</span></span>
<span data-ttu-id="33d84-128">Gibt den Pfad des wps_2 Skripts an, das die DSC-Konfiguration enthält, die von diesem Cmdlet importiert wird.</span><span class="sxs-lookup"><span data-stu-id="33d84-128">Specifies the path of the wps_2 script that contains the DSC configuration that this cmdlet imports.</span></span>

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

### <span data-ttu-id="33d84-129">-Tags</span><span class="sxs-lookup"><span data-stu-id="33d84-129">-Tags</span></span>
<span data-ttu-id="33d84-130">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="33d84-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="33d84-131">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="33d84-131">For example:</span></span>

<span data-ttu-id="33d84-132">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="33d84-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="33d84-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="33d84-133">-Confirm</span></span>
<span data-ttu-id="33d84-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="33d84-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33d84-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33d84-135">-WhatIf</span></span>
<span data-ttu-id="33d84-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="33d84-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33d84-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="33d84-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33d84-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33d84-138">-DefaultProfile</span></span>
<span data-ttu-id="33d84-139">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="33d84-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33d84-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33d84-140">CommonParameters</span></span>
<span data-ttu-id="33d84-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33d84-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33d84-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33d84-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33d84-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="33d84-143">INPUTS</span></span>

## <span data-ttu-id="33d84-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="33d84-144">OUTPUTS</span></span>

### <span data-ttu-id="33d84-145">Microsoft. Azure. Commands. Automation. Model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="33d84-145">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="33d84-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="33d84-146">NOTES</span></span>

## <span data-ttu-id="33d84-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="33d84-147">RELATED LINKS</span></span>

[<span data-ttu-id="33d84-148">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="33d84-148">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="33d84-149">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="33d84-149">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

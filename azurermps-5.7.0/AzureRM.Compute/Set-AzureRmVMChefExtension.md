---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: CC306D8C-A5EE-4655-B686-E5A77CCE5042
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMChefExtension.md
ms.openlocfilehash: 25ddfd3fcb7d087db493e87bdd9781b2bbb77040
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662365"
---
# <span data-ttu-id="a9242-101">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="a9242-101">Set-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="a9242-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9242-102">SYNOPSIS</span></span>
<span data-ttu-id="a9242-103">Fügt eine Erweiterung des Chefkochs zu einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="a9242-103">Adds a Chef extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9242-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9242-104">SYNTAX</span></span>

### <span data-ttu-id="a9242-105">Linux</span><span class="sxs-lookup"><span data-stu-id="a9242-105">Linux</span></span>
```
Set-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Linux] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9242-106">Windows</span><span class="sxs-lookup"><span data-stu-id="a9242-106">Windows</span></span>
```
Set-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Windows] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9242-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9242-107">DESCRIPTION</span></span>
<span data-ttu-id="a9242-108">Das Cmdlet " **Satz-AzureVMChefExtension** " fügt der virtuellen Maschine die Erweiterung "Chef" hinzu.</span><span class="sxs-lookup"><span data-stu-id="a9242-108">The **Set-AzureVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="a9242-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9242-109">EXAMPLES</span></span>

### <span data-ttu-id="a9242-110">Beispiel 1: Hinzufügen einer Chefkoch-Erweiterung zu einem virtuellen Windows-Computer</span><span class="sxs-lookup"><span data-stu-id="a9242-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Daemon "service" -SecretFile "C:\my_encrypted_data_bag_secret" -Windows
```

<span data-ttu-id="a9242-111">Mit diesem Befehl wird eine Erweiterung des Chefkochs zu einem virtuellen Windows-Computer mit dem Namen WindowsVM001 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a9242-111">This command adds a Chef extension to a Windows virtual machine named WindowsVM001.</span></span>
<span data-ttu-id="a9242-112">Wenn der virtuelle Computer gestartet wird, startet der Chefkoch den virtuellen Computer, um Apache auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a9242-112">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="a9242-113">Beispiel 2: Hinzufügen einer Chefkoch-Erweiterung zu einem virtuellen Linux-Computer</span><span class="sxs-lookup"><span data-stu-id="a9242-113">Example 2: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Secret "my_secret" -Linux
```

<span data-ttu-id="a9242-114">Mit diesem Befehl wird eine Erweiterung des Chefkochs zu einem virtuellen Linux-Computer mit dem Namen LinuxVM001 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a9242-114">This command adds a Chef extension to a Linux virtual machine named LinuxVM001.</span></span>
<span data-ttu-id="a9242-115">Wenn der virtuelle Computer gestartet wird, startet der Chefkoch den virtuellen Computer, um Apache auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a9242-115">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="a9242-116">Beispiel 3: Hinzufügen einer Chefkoch-Erweiterung zu einem virtuellen Windows-Computer mit Bootstrap-Optionen</span><span class="sxs-lookup"><span data-stu-id="a9242-116">Example 3: Add a Chef extension to a Windows virtual machine with bootstrap options</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup003" -VMName "WindowsVM002" -ValidationPem C:\my-org-validator.pem -ClientRb C:\client.rb -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows
```

<span data-ttu-id="a9242-117">Mit diesem Befehl wird die Erweiterung des Chefkochs zu einem virtuellen Windows-Computer mit dem Namen WindowsVM002 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a9242-117">This command adds the Chef extension to a Windows virtual machine named WindowsVM002.</span></span>
<span data-ttu-id="a9242-118">Wenn der virtuelle Computer gestartet wird, startet der Chefkoch den virtuellen Computer, um Apache auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a9242-118">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>
<span data-ttu-id="a9242-119">Nach dem Bootstrapping verweist der virtuelle Computer auf die im JSON-Format angegebenen bootstrapoptions.</span><span class="sxs-lookup"><span data-stu-id="a9242-119">After bootstrapping, the virtual machine refers to the BootstrapOptions specified in JSON format.</span></span>

## <span data-ttu-id="a9242-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9242-120">PARAMETERS</span></span>

### <span data-ttu-id="a9242-121">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="a9242-121">-AutoUpgradeMinorVersion</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9242-122">-Bootstrapoptions</span><span class="sxs-lookup"><span data-stu-id="a9242-122">-BootstrapOptions</span></span>
<span data-ttu-id="a9242-123">Gibt die Konfigurationseinstellungen in der Option client_rb an.</span><span class="sxs-lookup"><span data-stu-id="a9242-123">Specifies configuration settings in the client_rb option.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9242-124">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="a9242-124">-BootstrapVersion</span></span>
<span data-ttu-id="a9242-125">Gibt die Version der Bootstrap-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="a9242-125">Specifies the version of the bootstrap configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9242-126">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="a9242-126">-ChefDaemonInterval</span></span>
<span data-ttu-id="a9242-127">Gibt die Häufigkeit (in Minuten) an, auf der der Chef-Service ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a9242-127">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="a9242-128">Wenn Sie nicht möchten, dass der Chef-Service auf dem Azure VM installiert wird, setzen Sie in diesem Feld den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="a9242-128">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ChefServiceInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9242-129">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="a9242-129">-ChefServerUrl</span></span>
<span data-ttu-id="a9242-130">Gibt den Chefkoch-Server Link als URL an.</span><span class="sxs-lookup"><span data-stu-id="a9242-130">Specifies the Chef server link, as a URL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9242-131">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="a9242-131">-ClientRb</span></span>
<span data-ttu-id="a9242-132">Gibt den vollständigen Pfad des Chefkoch-Clients. RB an.</span><span class="sxs-lookup"><span data-stu-id="a9242-132">Specifies the full path of the Chef client.rb.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9242-133">-Daemon</span><span class="sxs-lookup"><span data-stu-id="a9242-133">-Daemon</span></span>
<span data-ttu-id="a9242-134">Konfiguriert den Chef-Client Dienst für die unbeaufsichtigte Ausführung.</span><span class="sxs-lookup"><span data-stu-id="a9242-134">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="a9242-135">Die Knoten Plattform sollte Windows sein.</span><span class="sxs-lookup"><span data-stu-id="a9242-135">The node platform should be Windows.</span></span>
<span data-ttu-id="a9242-136">Zulässige Optionen: "keine", "Dienst" und "Aufgabe".</span><span class="sxs-lookup"><span data-stu-id="a9242-136">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="a9242-137">keine – zurzeit wird verhindert, dass der Chef-Client-Dienst als Dienst konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="a9242-137">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="a9242-138">Dienst – konfiguriert den Chef-Client so, dass er automatisch im Hintergrund als Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a9242-138">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="a9242-139">Aufgabe – konfiguriert den Chef-Client so, dass er automatisch im Hintergrund als secheduled-Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a9242-139">task - Configures the chef-client to run automatically in the background as a secheduled task.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: none, service, task

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9242-140">-Jsonattribute</span><span class="sxs-lookup"><span data-stu-id="a9242-140">-JsonAttribute</span></span>
<span data-ttu-id="a9242-141">Eine JSON-Zeichenfolge, die der ersten Ausführung von Chef-Client hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9242-141">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="a9242-142">beispielsweise-jsonattribute ' {"foo": "Leiste"} '</span><span class="sxs-lookup"><span data-stu-id="a9242-142">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9242-143">-Linux</span><span class="sxs-lookup"><span data-stu-id="a9242-143">-Linux</span></span>
<span data-ttu-id="a9242-144">Gibt an, dass dieses Cmdlet einen virtuellen Windows-Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="a9242-144">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9242-145">-Standort</span><span class="sxs-lookup"><span data-stu-id="a9242-145">-Location</span></span>
<span data-ttu-id="a9242-146">Gibt den Speicherort der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="a9242-146">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9242-147">-Name</span><span class="sxs-lookup"><span data-stu-id="a9242-147">-Name</span></span>
<span data-ttu-id="a9242-148">Gibt den Namen der Erweiterung "Chef" an.</span><span class="sxs-lookup"><span data-stu-id="a9242-148">Specifies the name of the Chef extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9242-149">-OrganizationName</span><span class="sxs-lookup"><span data-stu-id="a9242-149">-OrganizationName</span></span>
<span data-ttu-id="a9242-150">Gibt den Organisationsnamen der Erweiterung "Chef" an.</span><span class="sxs-lookup"><span data-stu-id="a9242-150">Specifies the organization name of the Chef extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9242-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9242-151">-ResourceGroupName</span></span>
<span data-ttu-id="a9242-152">Gibt den Namen der Ressourcengruppe an, die den virtuellen Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="a9242-152">Specifies the name of the resource group that contains the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9242-153">-RunList</span><span class="sxs-lookup"><span data-stu-id="a9242-153">-RunList</span></span>
<span data-ttu-id="a9242-154">Gibt die Liste "Leiter Knoten ausführen" an.</span><span class="sxs-lookup"><span data-stu-id="a9242-154">Specifies the Chef node run list.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9242-155">-Secret</span><span class="sxs-lookup"><span data-stu-id="a9242-155">-Secret</span></span>
<span data-ttu-id="a9242-156">Der Verschlüsselungsschlüssel, der zum Verschlüsseln und Entschlüsseln der Daten Beutel-Elementwerte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a9242-156">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9242-157">-Secretdatei</span><span class="sxs-lookup"><span data-stu-id="a9242-157">-SecretFile</span></span>
<span data-ttu-id="a9242-158">Der Pfad zu der Datei, die den Verschlüsselungsschlüssel enthält, der zum Verschlüsseln und Entschlüsseln der Daten Beutel-Elementwerte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a9242-158">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9242-159">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="a9242-159">-TypeHandlerVersion</span></span>
<span data-ttu-id="a9242-160">Gibt die Version der Erweiterung an, die für diesen virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9242-160">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9242-161">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="a9242-161">-ValidationClientName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9242-162">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="a9242-162">-ValidationPem</span></span>
<span data-ttu-id="a9242-163">Gibt den "Chef Validator. PEM"-Dateipfad an</span><span class="sxs-lookup"><span data-stu-id="a9242-163">Specifies the Chef validator .pem file path</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9242-164">-VMName</span><span class="sxs-lookup"><span data-stu-id="a9242-164">-VMName</span></span>
<span data-ttu-id="a9242-165">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="a9242-165">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="a9242-166">Mit diesem Cmdlet wird die Erweiterung "Chef" für den virtuellen Computer, den dieser Parameter angibt, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a9242-166">This cmdlet adds the Chef extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9242-167">-Windows</span><span class="sxs-lookup"><span data-stu-id="a9242-167">-Windows</span></span>
<span data-ttu-id="a9242-168">Gibt an, dass dieses Cmdlet einen virtuellen Windows-Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="a9242-168">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9242-169">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a9242-169">-Confirm</span></span>
<span data-ttu-id="a9242-170">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a9242-170">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9242-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9242-171">-WhatIf</span></span>
<span data-ttu-id="a9242-172">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a9242-172">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="a9242-173">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a9242-173">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9242-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9242-174">CommonParameters</span></span>
<span data-ttu-id="a9242-175">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9242-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9242-176">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9242-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9242-177">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9242-177">INPUTS</span></span>

### <span data-ttu-id="a9242-178">Keine</span><span class="sxs-lookup"><span data-stu-id="a9242-178">None</span></span>
<span data-ttu-id="a9242-179">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="a9242-179">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a9242-180">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9242-180">OUTPUTS</span></span>

## <span data-ttu-id="a9242-181">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9242-181">NOTES</span></span>

## <span data-ttu-id="a9242-182">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9242-182">RELATED LINKS</span></span>

[<span data-ttu-id="a9242-183">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="a9242-183">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="a9242-184">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="a9242-184">Remove-AzureRmVMChefExtension</span></span>](./Remove-AzureRmVMChefExtension.md)

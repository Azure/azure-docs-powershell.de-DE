---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: CC306D8C-A5EE-4655-B686-E5A77CCE5042
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMChefExtension.md
ms.openlocfilehash: 3bedeb243b79cada713889145771d45511cb7b7f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844239"
---
# <span data-ttu-id="a2298-101">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="a2298-101">Set-AzVMChefExtension</span></span>

## <span data-ttu-id="a2298-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a2298-102">SYNOPSIS</span></span>
<span data-ttu-id="a2298-103">Fügt eine Erweiterung des Chefkochs zu einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="a2298-103">Adds a Chef extension to a virtual machine.</span></span>

## <span data-ttu-id="a2298-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2298-104">SYNTAX</span></span>

### <span data-ttu-id="a2298-105">Linux</span><span class="sxs-lookup"><span data-stu-id="a2298-105">Linux</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Linux] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2298-106">Windows</span><span class="sxs-lookup"><span data-stu-id="a2298-106">Windows</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Windows] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a2298-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a2298-107">DESCRIPTION</span></span>
<span data-ttu-id="a2298-108">Das Cmdlet " **Satz-AzureVMChefExtension** " fügt der virtuellen Maschine die Erweiterung "Chef" hinzu.</span><span class="sxs-lookup"><span data-stu-id="a2298-108">The **Set-AzureVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="a2298-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a2298-109">EXAMPLES</span></span>

### <span data-ttu-id="a2298-110">Beispiel 1: Hinzufügen einer Chefkoch-Erweiterung zu einem virtuellen Windows-Computer</span><span class="sxs-lookup"><span data-stu-id="a2298-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Daemon "service" -SecretFile "C:\my_encrypted_data_bag_secret" -Windows
```

<span data-ttu-id="a2298-111">Mit diesem Befehl wird eine Erweiterung des Chefkochs zu einem virtuellen Windows-Computer mit dem Namen WindowsVM001 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a2298-111">This command adds a Chef extension to a Windows virtual machine named WindowsVM001.</span></span>
<span data-ttu-id="a2298-112">Wenn der virtuelle Computer gestartet wird, startet der Chefkoch den virtuellen Computer, um Apache auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a2298-112">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="a2298-113">Beispiel 2: Hinzufügen einer Chefkoch-Erweiterung zu einem virtuellen Linux-Computer</span><span class="sxs-lookup"><span data-stu-id="a2298-113">Example 2: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Secret "my_secret" -Linux
```

<span data-ttu-id="a2298-114">Mit diesem Befehl wird eine Erweiterung des Chefkochs zu einem virtuellen Linux-Computer mit dem Namen LinuxVM001 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a2298-114">This command adds a Chef extension to a Linux virtual machine named LinuxVM001.</span></span>
<span data-ttu-id="a2298-115">Wenn der virtuelle Computer gestartet wird, startet der Chefkoch den virtuellen Computer, um Apache auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a2298-115">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="a2298-116">Beispiel 3: Hinzufügen einer Chefkoch-Erweiterung zu einem virtuellen Windows-Computer mit Bootstrap-Optionen</span><span class="sxs-lookup"><span data-stu-id="a2298-116">Example 3: Add a Chef extension to a Windows virtual machine with bootstrap options</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup003" -VMName "WindowsVM002" -ValidationPem C:\my-org-validator.pem -ClientRb C:\client.rb -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows
```

<span data-ttu-id="a2298-117">Mit diesem Befehl wird die Erweiterung des Chefkochs zu einem virtuellen Windows-Computer mit dem Namen WindowsVM002 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a2298-117">This command adds the Chef extension to a Windows virtual machine named WindowsVM002.</span></span>
<span data-ttu-id="a2298-118">Wenn der virtuelle Computer gestartet wird, startet der Chefkoch den virtuellen Computer, um Apache auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a2298-118">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>
<span data-ttu-id="a2298-119">Nach dem Bootstrapping verweist der virtuelle Computer auf die im JSON-Format angegebenen bootstrapoptions.</span><span class="sxs-lookup"><span data-stu-id="a2298-119">After bootstrapping, the virtual machine refers to the BootstrapOptions specified in JSON format.</span></span>

## <span data-ttu-id="a2298-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2298-120">PARAMETERS</span></span>

### <span data-ttu-id="a2298-121">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="a2298-121">-AutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="a2298-122">-Bootstrapoptions</span><span class="sxs-lookup"><span data-stu-id="a2298-122">-BootstrapOptions</span></span>
<span data-ttu-id="a2298-123">Gibt die Konfigurationseinstellungen in der Option client_rb an.</span><span class="sxs-lookup"><span data-stu-id="a2298-123">Specifies configuration settings in the client_rb option.</span></span>

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

### <span data-ttu-id="a2298-124">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="a2298-124">-BootstrapVersion</span></span>
<span data-ttu-id="a2298-125">Gibt die Version der Bootstrap-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="a2298-125">Specifies the version of the bootstrap configuration.</span></span>

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

### <span data-ttu-id="a2298-126">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="a2298-126">-ChefDaemonInterval</span></span>
<span data-ttu-id="a2298-127">Gibt die Häufigkeit (in Minuten) an, auf der der Chef-Service ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a2298-127">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="a2298-128">Wenn Sie nicht möchten, dass der Chef-Service auf dem Azure VM installiert wird, setzen Sie in diesem Feld den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="a2298-128">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

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

### <span data-ttu-id="a2298-129">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="a2298-129">-ChefServerUrl</span></span>
<span data-ttu-id="a2298-130">Gibt den Chefkoch-Server Link als URL an.</span><span class="sxs-lookup"><span data-stu-id="a2298-130">Specifies the Chef server link, as a URL.</span></span>

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

### <span data-ttu-id="a2298-131">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="a2298-131">-ClientRb</span></span>
<span data-ttu-id="a2298-132">Gibt den vollständigen Pfad des Chefkoch-Clients. RB an.</span><span class="sxs-lookup"><span data-stu-id="a2298-132">Specifies the full path of the Chef client.rb.</span></span>

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

### <span data-ttu-id="a2298-133">-Daemon</span><span class="sxs-lookup"><span data-stu-id="a2298-133">-Daemon</span></span>
<span data-ttu-id="a2298-134">Konfiguriert den Chef-Client Dienst für die unbeaufsichtigte Ausführung.</span><span class="sxs-lookup"><span data-stu-id="a2298-134">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="a2298-135">Die Knoten Plattform sollte Windows sein.</span><span class="sxs-lookup"><span data-stu-id="a2298-135">The node platform should be Windows.</span></span>
<span data-ttu-id="a2298-136">Zulässige Optionen: "keine", "Dienst" und "Aufgabe".</span><span class="sxs-lookup"><span data-stu-id="a2298-136">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="a2298-137">keine – zurzeit wird verhindert, dass der Chef-Client-Dienst als Dienst konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="a2298-137">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="a2298-138">Dienst – konfiguriert den Chef-Client so, dass er automatisch im Hintergrund als Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a2298-138">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="a2298-139">Aufgabe – konfiguriert den Chef-Client so, dass er automatisch im Hintergrund als secheduled-Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a2298-139">task - Configures the chef-client to run automatically in the background as a secheduled task.</span></span>

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

### <span data-ttu-id="a2298-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2298-140">-DefaultProfile</span></span>
<span data-ttu-id="a2298-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a2298-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2298-142">-Jsonattribute</span><span class="sxs-lookup"><span data-stu-id="a2298-142">-JsonAttribute</span></span>
<span data-ttu-id="a2298-143">Eine JSON-Zeichenfolge, die der ersten Ausführung von Chef-Client hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2298-143">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="a2298-144">beispielsweise-jsonattribute ' {"foo": "Leiste"} '</span><span class="sxs-lookup"><span data-stu-id="a2298-144">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

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

### <span data-ttu-id="a2298-145">-Linux</span><span class="sxs-lookup"><span data-stu-id="a2298-145">-Linux</span></span>
<span data-ttu-id="a2298-146">Gibt an, dass dieses Cmdlet einen virtuellen Windows-Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="a2298-146">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="a2298-147">-Standort</span><span class="sxs-lookup"><span data-stu-id="a2298-147">-Location</span></span>
<span data-ttu-id="a2298-148">Gibt den Speicherort der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="a2298-148">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="a2298-149">-Name</span><span class="sxs-lookup"><span data-stu-id="a2298-149">-Name</span></span>
<span data-ttu-id="a2298-150">Gibt den Namen der Erweiterung "Chef" an.</span><span class="sxs-lookup"><span data-stu-id="a2298-150">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="a2298-151">-OrganizationName</span><span class="sxs-lookup"><span data-stu-id="a2298-151">-OrganizationName</span></span>
<span data-ttu-id="a2298-152">Gibt den Organisationsnamen der Erweiterung "Chef" an.</span><span class="sxs-lookup"><span data-stu-id="a2298-152">Specifies the organization name of the Chef extension.</span></span>

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

### <span data-ttu-id="a2298-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2298-153">-ResourceGroupName</span></span>
<span data-ttu-id="a2298-154">Gibt den Namen der Ressourcengruppe an, die den virtuellen Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="a2298-154">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="a2298-155">-RunList</span><span class="sxs-lookup"><span data-stu-id="a2298-155">-RunList</span></span>
<span data-ttu-id="a2298-156">Gibt die Liste "Leiter Knoten ausführen" an.</span><span class="sxs-lookup"><span data-stu-id="a2298-156">Specifies the Chef node run list.</span></span>

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

### <span data-ttu-id="a2298-157">-Secret</span><span class="sxs-lookup"><span data-stu-id="a2298-157">-Secret</span></span>
<span data-ttu-id="a2298-158">Der Verschlüsselungsschlüssel, der zum Verschlüsseln und Entschlüsseln der Daten Beutel-Elementwerte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a2298-158">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="a2298-159">-Secretdatei</span><span class="sxs-lookup"><span data-stu-id="a2298-159">-SecretFile</span></span>
<span data-ttu-id="a2298-160">Der Pfad zu der Datei, die den Verschlüsselungsschlüssel enthält, der zum Verschlüsseln und Entschlüsseln der Daten Beutel-Elementwerte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a2298-160">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="a2298-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="a2298-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="a2298-162">Gibt die Version der Erweiterung an, die für diesen virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2298-162">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="a2298-163">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="a2298-163">-ValidationClientName</span></span>
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

### <span data-ttu-id="a2298-164">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="a2298-164">-ValidationPem</span></span>
<span data-ttu-id="a2298-165">Gibt den "Chef Validator. PEM"-Dateipfad an</span><span class="sxs-lookup"><span data-stu-id="a2298-165">Specifies the Chef validator .pem file path</span></span>

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

### <span data-ttu-id="a2298-166">-VMName</span><span class="sxs-lookup"><span data-stu-id="a2298-166">-VMName</span></span>
<span data-ttu-id="a2298-167">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="a2298-167">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="a2298-168">Mit diesem Cmdlet wird die Erweiterung "Chef" für den virtuellen Computer, den dieser Parameter angibt, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a2298-168">This cmdlet adds the Chef extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="a2298-169">-Windows</span><span class="sxs-lookup"><span data-stu-id="a2298-169">-Windows</span></span>
<span data-ttu-id="a2298-170">Gibt an, dass dieses Cmdlet einen virtuellen Windows-Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="a2298-170">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="a2298-171">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a2298-171">-Confirm</span></span>
<span data-ttu-id="a2298-172">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a2298-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2298-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2298-173">-WhatIf</span></span>
<span data-ttu-id="a2298-174">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a2298-174">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="a2298-175">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a2298-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2298-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2298-176">CommonParameters</span></span>
<span data-ttu-id="a2298-177">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2298-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2298-178">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2298-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2298-179">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a2298-179">INPUTS</span></span>

### <span data-ttu-id="a2298-180">Keine</span><span class="sxs-lookup"><span data-stu-id="a2298-180">None</span></span>
<span data-ttu-id="a2298-181">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="a2298-181">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a2298-182">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a2298-182">OUTPUTS</span></span>

### <span data-ttu-id="a2298-183">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a2298-183">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a2298-184">Notizen</span><span class="sxs-lookup"><span data-stu-id="a2298-184">NOTES</span></span>

## <span data-ttu-id="a2298-185">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a2298-185">RELATED LINKS</span></span>

[<span data-ttu-id="a2298-186">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="a2298-186">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="a2298-187">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="a2298-187">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)

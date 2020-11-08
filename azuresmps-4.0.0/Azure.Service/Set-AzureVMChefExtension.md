---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 021D4624-AE78-4FBE-B1DE-A8A84DF1FC90
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52c3a26887e42884025234ba5f1a7330c258e903
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006251"
---
# <span data-ttu-id="9191f-101">Set-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="9191f-101">Set-AzureVMChefExtension</span></span>

## <span data-ttu-id="9191f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9191f-102">SYNOPSIS</span></span>
<span data-ttu-id="9191f-103">Fügt dem virtuellen Computer die Erweiterung "Chef" hinzu.</span><span class="sxs-lookup"><span data-stu-id="9191f-103">Adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="9191f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9191f-104">SYNTAX</span></span>

### <span data-ttu-id="9191f-105">Windows (Standard)</span><span class="sxs-lookup"><span data-stu-id="9191f-105">Windows (Default)</span></span>
```
Set-AzureVMChefExtension [-Version <String>] -ValidationPem <String> [-ClientRb <String>]
 [-BootstrapOptions <String>] [-RunList <String>] [-JsonAttribute <String>] [-ChefDaemonInterval <String>]
 [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>] [-Windows]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9191f-106">Linux</span><span class="sxs-lookup"><span data-stu-id="9191f-106">Linux</span></span>
```
Set-AzureVMChefExtension [-Version <String>] -ValidationPem <String> [-ClientRb <String>]
 [-BootstrapOptions <String>] [-RunList <String>] [-JsonAttribute <String>] [-ChefDaemonInterval <String>]
 [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>] [-Linux]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9191f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9191f-107">DESCRIPTION</span></span>
<span data-ttu-id="9191f-108">Das Cmdlet " **Satz-AzureVMChefExtension** " fügt der virtuellen Maschine die Erweiterung "Chef" hinzu.</span><span class="sxs-lookup"><span data-stu-id="9191f-108">The **Set-AzureVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="9191f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9191f-109">EXAMPLES</span></span>

### <span data-ttu-id="9191f-110">Beispiel 1: Hinzufügen einer Chefkoch-Erweiterung zu einem virtuellen Windows-Computer</span><span class="sxs-lookup"><span data-stu-id="9191f-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ClientRb "C:\\client.rb" -RunList "Apache" -Windows;
```

<span data-ttu-id="9191f-111">Mit diesem Befehl wird eine Erweiterung des Chefkochs zu einem virtuellen Windows-Computer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9191f-111">This command adds a Chef extension to a Windows virtual machine.</span></span>
<span data-ttu-id="9191f-112">Wenn die virtuelle Maschine auftaucht, ist Sie bootstrapped mit dem Chefkoch und führt Apache auf Sie.</span><span class="sxs-lookup"><span data-stu-id="9191f-112">When the virtual machine comes up, it is bootstrapped with Chef and runs Apache on it.</span></span>

### <span data-ttu-id="9191f-113">Beispiel 2: Hinzufügen einer Chefkoch-Erweiterung zu einem virtuellen Windows-Computer mit Bootstrapping</span><span class="sxs-lookup"><span data-stu-id="9191f-113">Example 2: Add a Chef extension to a Windows virtual machine with bootstrapping</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows;
```

<span data-ttu-id="9191f-114">Mit diesem Befehl wird die Erweiterung des Chefkochs zu einem virtuellen Windows-Computer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9191f-114">This command adds the Chef extension to a Windows virtual machine.</span></span>
<span data-ttu-id="9191f-115">Wenn die virtuelle Maschine gestartet wird, ist Sie bootstrapped mit dem Chefkoch und führt Apache darauf aus.</span><span class="sxs-lookup"><span data-stu-id="9191f-115">When the virtual machine launches, it is bootstrapped with Chef and runs Apache on it.</span></span>
<span data-ttu-id="9191f-116">Nach dem Bootstrapping verweist der virtuelle Computer auf die im JSON-Format angegebenen *bootstrapoptions* .</span><span class="sxs-lookup"><span data-stu-id="9191f-116">After bootstrapping, the virtual machine refers to the *BootstrapOptions* specified in JSON format.</span></span>

### <span data-ttu-id="9191f-117">Beispiel 3: Hinzufügen einer Erweiterung des Chefkochs zu einem virtuellen Windows-Computer und Installieren von Apache und git</span><span class="sxs-lookup"><span data-stu-id="9191f-117">Example 3: Add a Chef extension to a Windows virtual machine and install Apache and GIT</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ChefServerUrl "http://ipaddress:port" -ValidationClientName "MyOrg-Validator" -RunList "apache, git" -Windows;
```

<span data-ttu-id="9191f-118">Mit diesem Befehl wird die Erweiterung des Chefkochs zu einem virtuellen Windows-Computer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9191f-118">This command adds the Chef extension to a Windows virtual machine.</span></span>
<span data-ttu-id="9191f-119">Wenn die virtuelle Maschine gestartet wird, ist Sie mit dem Chefkoch bootstrapped und hat Apache und Git installiert.</span><span class="sxs-lookup"><span data-stu-id="9191f-119">When the virtual machine launches, it is bootstrapped with Chef and have Apache and GIT installed.</span></span>
<span data-ttu-id="9191f-120">Wenn Sie den Client. RB nicht angeben, müssen Sie den Chefkoch-Server-URL und den Namen des Validierungs Clients angeben.</span><span class="sxs-lookup"><span data-stu-id="9191f-120">If you do not provide the client.rb, you need to provide the Chef server URL and validation client name.</span></span>

### <span data-ttu-id="9191f-121">Beispiel 4: Hinzufügen einer Chefkoch-Erweiterung zu einem virtuellen Linux-Computer</span><span class="sxs-lookup"><span data-stu-id="9191f-121">Example 4: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ChefServerUrl "http://ipaddress:port" -OrganizationName "MyOrg" -Linux;
```

<span data-ttu-id="9191f-122">Mit diesem Befehl wird die Erweiterung des Chefkochs zu einem virtuellen Linux-Computer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9191f-122">This command adds the Chef extension to a Linux virtual machine.</span></span>
<span data-ttu-id="9191f-123">Wenn die virtuelle Maschine gestartet wird, ist Sie bootstrapped mit dem Chefkoch.</span><span class="sxs-lookup"><span data-stu-id="9191f-123">When the virtual machine launches, it is bootstrapped with Chef.</span></span>
<span data-ttu-id="9191f-124">Wenn Sie den Client. RB nicht angeben, müssen Sie die Server-URL und die Organisation des Chefkochs angeben.</span><span class="sxs-lookup"><span data-stu-id="9191f-124">If you do not provide the client.rb, you need to provide the Chef server URL and organization.</span></span>

## <span data-ttu-id="9191f-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="9191f-125">PARAMETERS</span></span>

### <span data-ttu-id="9191f-126">-Bootstrapoptions</span><span class="sxs-lookup"><span data-stu-id="9191f-126">-BootstrapOptions</span></span>
<span data-ttu-id="9191f-127">Gibt Bootstrap-Optionen im JSON-Format (JavaScript Object Notation) an.</span><span class="sxs-lookup"><span data-stu-id="9191f-127">Specifies bootstrap options in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="9191f-128">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="9191f-128">-BootstrapVersion</span></span>
<span data-ttu-id="9191f-129">Gibt die Version des Chefkoch-Clients an, die zusammen mit der Erweiterung installiert wird.</span><span class="sxs-lookup"><span data-stu-id="9191f-129">Specifies the version of the Chef client that is installed together with the extension.</span></span>

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

### <span data-ttu-id="9191f-130">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="9191f-130">-ChefDaemonInterval</span></span>
<span data-ttu-id="9191f-131">Gibt die Häufigkeit (in Minuten) an, auf der der Chef-Service ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9191f-131">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="9191f-132">Wenn Sie nicht möchten, dass der Chef-Service auf dem Azure VM installiert wird, setzen Sie in diesem Feld den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="9191f-132">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

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

### <span data-ttu-id="9191f-133">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="9191f-133">-ChefServerUrl</span></span>
<span data-ttu-id="9191f-134">Gibt die URL des Chef Servers an.</span><span class="sxs-lookup"><span data-stu-id="9191f-134">Specifies the URL of the Chef server.</span></span>

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

### <span data-ttu-id="9191f-135">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="9191f-135">-ClientRb</span></span>
<span data-ttu-id="9191f-136">Gibt den vollständigen Pfad des Chefkoch-Clients. RB an.</span><span class="sxs-lookup"><span data-stu-id="9191f-136">Specifies the full path of the Chef client.rb.</span></span>

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

### <span data-ttu-id="9191f-137">-Daemon</span><span class="sxs-lookup"><span data-stu-id="9191f-137">-Daemon</span></span>
<span data-ttu-id="9191f-138">Konfiguriert den Chef-Client Dienst für die unbeaufsichtigte Ausführung.</span><span class="sxs-lookup"><span data-stu-id="9191f-138">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="9191f-139">Die Knoten Plattform sollte Windows sein.</span><span class="sxs-lookup"><span data-stu-id="9191f-139">The node platform should be Windows.</span></span>
<span data-ttu-id="9191f-140">Zulässige Optionen: "keine", "Dienst" und "Aufgabe".</span><span class="sxs-lookup"><span data-stu-id="9191f-140">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="9191f-141">keine – zurzeit wird verhindert, dass der Chef-Client-Dienst als Dienst konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="9191f-141">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="9191f-142">Dienst – konfiguriert den Chef-Client so, dass er automatisch im Hintergrund als Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9191f-142">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="9191f-143">Aufgabe – konfiguriert den Chef-Client so, dass er automatisch im Hintergrund als secheduled-Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9191f-143">task - Configures the chef-client to run automatically in the background as a secheduled task.</span></span>

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

### <span data-ttu-id="9191f-144">-Information</span><span class="sxs-lookup"><span data-stu-id="9191f-144">-InformationAction</span></span>
<span data-ttu-id="9191f-145">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="9191f-145">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9191f-146">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9191f-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9191f-147">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="9191f-147">Continue</span></span>
- <span data-ttu-id="9191f-148">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="9191f-148">Ignore</span></span>
- <span data-ttu-id="9191f-149">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="9191f-149">Inquire</span></span>
- <span data-ttu-id="9191f-150">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9191f-150">SilentlyContinue</span></span>
- <span data-ttu-id="9191f-151">Beenden</span><span class="sxs-lookup"><span data-stu-id="9191f-151">Stop</span></span>
- <span data-ttu-id="9191f-152">Anhalten</span><span class="sxs-lookup"><span data-stu-id="9191f-152">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9191f-153">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9191f-153">-InformationVariable</span></span>
<span data-ttu-id="9191f-154">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="9191f-154">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9191f-155">-Jsonattribute</span><span class="sxs-lookup"><span data-stu-id="9191f-155">-JsonAttribute</span></span>
<span data-ttu-id="9191f-156">Eine JSON-Zeichenfolge, die der ersten Ausführung von Chef-Client hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9191f-156">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="9191f-157">beispielsweise-jsonattribute ' {"foo": "Leiste"} '</span><span class="sxs-lookup"><span data-stu-id="9191f-157">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

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

### <span data-ttu-id="9191f-158">-Linux</span><span class="sxs-lookup"><span data-stu-id="9191f-158">-Linux</span></span>
<span data-ttu-id="9191f-159">Gibt an, dass mit diesem Cmdlet ein Linux-basierter virtueller Computer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="9191f-159">Indicates that this cmdlet creates a Linux based virtual machine.</span></span>

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

### <span data-ttu-id="9191f-160">-OrganizationName</span><span class="sxs-lookup"><span data-stu-id="9191f-160">-OrganizationName</span></span>
<span data-ttu-id="9191f-161">Gibt den Organisationsnamen der Erweiterung "Chef" an.</span><span class="sxs-lookup"><span data-stu-id="9191f-161">Specifies the organization name of the Chef extension.</span></span>

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

### <span data-ttu-id="9191f-162">-Profil</span><span class="sxs-lookup"><span data-stu-id="9191f-162">-Profile</span></span>
<span data-ttu-id="9191f-163">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="9191f-163">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9191f-164">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="9191f-164">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9191f-165">-RunList</span><span class="sxs-lookup"><span data-stu-id="9191f-165">-RunList</span></span>
<span data-ttu-id="9191f-166">Gibt die Liste "Leiter Knoten ausführen" an.</span><span class="sxs-lookup"><span data-stu-id="9191f-166">Specifies the Chef node run list.</span></span>

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

### <span data-ttu-id="9191f-167">-Secret</span><span class="sxs-lookup"><span data-stu-id="9191f-167">-Secret</span></span>
<span data-ttu-id="9191f-168">Der Verschlüsselungsschlüssel, der zum Verschlüsseln und Entschlüsseln der Daten Beutel-Elementwerte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9191f-168">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="9191f-169">-Secretdatei</span><span class="sxs-lookup"><span data-stu-id="9191f-169">-SecretFile</span></span>
<span data-ttu-id="9191f-170">Der Pfad zu der Datei, die den Verschlüsselungsschlüssel enthält, der zum Verschlüsseln und Entschlüsseln der Daten Beutel-Elementwerte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9191f-170">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="9191f-171">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="9191f-171">-ValidationClientName</span></span>
<span data-ttu-id="9191f-172">Gibt den Namen des Validierungs Clients an.</span><span class="sxs-lookup"><span data-stu-id="9191f-172">Specifies the name of the validation client.</span></span>

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

### <span data-ttu-id="9191f-173">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="9191f-173">-ValidationPem</span></span>
<span data-ttu-id="9191f-174">Gibt den Datei Pfad des Chefkochs Validator. PEM an.</span><span class="sxs-lookup"><span data-stu-id="9191f-174">Specifies the Chef validator .pem file path.</span></span>

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

### <span data-ttu-id="9191f-175">-Version</span><span class="sxs-lookup"><span data-stu-id="9191f-175">-Version</span></span>
<span data-ttu-id="9191f-176">Gibt die Versionsnummer der Erweiterung "Chef" an.</span><span class="sxs-lookup"><span data-stu-id="9191f-176">Specifies the version number of the Chef extension.</span></span>

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

### <span data-ttu-id="9191f-177">-VM</span><span class="sxs-lookup"><span data-stu-id="9191f-177">-VM</span></span>
<span data-ttu-id="9191f-178">Gibt das Objekt des beständigen virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="9191f-178">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9191f-179">-Windows</span><span class="sxs-lookup"><span data-stu-id="9191f-179">-Windows</span></span>
<span data-ttu-id="9191f-180">Gibt an, dass dieses Cmdlet einen virtuellen Windows-Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="9191f-180">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="9191f-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9191f-181">CommonParameters</span></span>
<span data-ttu-id="9191f-182">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9191f-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9191f-183">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9191f-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9191f-184">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9191f-184">INPUTS</span></span>

## <span data-ttu-id="9191f-185">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9191f-185">OUTPUTS</span></span>

## <span data-ttu-id="9191f-186">Notizen</span><span class="sxs-lookup"><span data-stu-id="9191f-186">NOTES</span></span>

## <span data-ttu-id="9191f-187">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9191f-187">RELATED LINKS</span></span>

[<span data-ttu-id="9191f-188">Get-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="9191f-188">Get-AzureVMChefExtension</span></span>](./Get-AzureVMChefExtension.md)

[<span data-ttu-id="9191f-189">Remove-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="9191f-189">Remove-AzureVMChefExtension</span></span>](./Remove-AzureVMChefExtension.md)



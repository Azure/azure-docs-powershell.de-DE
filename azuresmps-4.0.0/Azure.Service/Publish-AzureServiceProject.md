---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CF7E7C62-88FC-48CA-940F-9A6C7442BEF2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8166cd3faa951171dd3ac865b17b8a03bcefdd45
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006089"
---
# <span data-ttu-id="93b8c-101">Publish-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="93b8c-101">Publish-AzureServiceProject</span></span>

## <span data-ttu-id="93b8c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="93b8c-102">SYNOPSIS</span></span>
<span data-ttu-id="93b8c-103">Veröffentlichen Sie den aktuellen Dienst in Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="93b8c-103">Publish the current service to Windows Azure.</span></span>

## <span data-ttu-id="93b8c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="93b8c-104">SYNTAX</span></span>

### <span data-ttu-id="93b8c-105">PublishFromServiceDefinition (Standard)</span><span class="sxs-lookup"><span data-stu-id="93b8c-105">PublishFromServiceDefinition (Default)</span></span>
```
Publish-AzureServiceProject [-ServiceName <String>] [-StorageAccountName <String>] [-Location <String>]
 [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>] [-ForceUpgrade]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="93b8c-106">PublishFromPackage</span><span class="sxs-lookup"><span data-stu-id="93b8c-106">PublishFromPackage</span></span>
```
Publish-AzureServiceProject [-Package <String>] -Configuration <String> [-StorageAccountName <String>]
 [-Location <String>] [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>]
 [-ForceUpgrade] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="93b8c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93b8c-107">DESCRIPTION</span></span>
<span data-ttu-id="93b8c-108">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="93b8c-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="93b8c-109">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="93b8c-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="93b8c-110">Mit dem Cmdlet " **Publish-AzureServiceProject** " wird der aktuelle Dienst in der Cloud veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="93b8c-110">The **Publish-AzureServiceProject** cmdlet publishes the current service to the cloud.</span></span>
<span data-ttu-id="93b8c-111">Sie können die Veröffentlichungskonfiguration (wie **Abonnement** , **StorageAccountName** , **Speicherort** , **Steckplatz** ) in der Befehlszeile oder in den lokalen Einstellungen über das Cmdlet " **Satz-AzureServiceProject** " angeben.</span><span class="sxs-lookup"><span data-stu-id="93b8c-111">You can specify publishing configuration (such as **Subscription** , **StorageAccountName** , **Location** , **Slot** ) on the command line, or in local settings through the **Set-AzureServiceProject** cmdlet.</span></span>

## <span data-ttu-id="93b8c-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="93b8c-112">EXAMPLES</span></span>

### <span data-ttu-id="93b8c-113">Beispiel 1: Veröffentlichen eines Dienstprojekts mit Standardwerten</span><span class="sxs-lookup"><span data-stu-id="93b8c-113">Example 1: Publish a service project with default values</span></span>
```
PS C:\> Publish-AzureServiceProject
```

<span data-ttu-id="93b8c-114">In diesem Beispiel wird der aktuelle Dienst unter Verwendung der aktuellen Diensteinstellungen und des aktuellen Azure Publish-Profils veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="93b8c-114">This example publishes the current service, using the current service settings and the current Azure publish profile.</span></span>

### <span data-ttu-id="93b8c-115">Beispiel 2: Erstellen eines Bereitstellungspakets</span><span class="sxs-lookup"><span data-stu-id="93b8c-115">Example 2: Create a deployment package</span></span>
```
PS C:\> Publish-AzureServiceProject -PackageOnly
```

<span data-ttu-id="93b8c-116">In diesem Beispiel wird eine Bereitstellungspaket Datei (cspkg) im Dienstverzeichnis erstellt und nicht in Windows Azure veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="93b8c-116">This example creates a deployment package (.cspkg) file in the service directory and does not publish to Windows Azure.</span></span>

## <span data-ttu-id="93b8c-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="93b8c-117">PARAMETERS</span></span>

### <span data-ttu-id="93b8c-118">-Affinitygroup</span><span class="sxs-lookup"><span data-stu-id="93b8c-118">-AffinityGroup</span></span>
<span data-ttu-id="93b8c-119">Gibt die affinitätsgruppe an, die der Dienst verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="93b8c-119">Specifies the affinity group that you want the service to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93b8c-120">-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="93b8c-120">-Configuration</span></span>
<span data-ttu-id="93b8c-121">Gibt die Konfigurationsdatei des Diensts an.</span><span class="sxs-lookup"><span data-stu-id="93b8c-121">Specifies the service configuration file.</span></span>
<span data-ttu-id="93b8c-122">Wenn Sie diesen Parameter angeben, geben Sie den *Package* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="93b8c-122">If you specify this parameter, specify the *Package* parameter.</span></span>

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: cc

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93b8c-123">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="93b8c-123">-DeploymentName</span></span>
<span data-ttu-id="93b8c-124">Gibt den Bereitstellungsnamen an.</span><span class="sxs-lookup"><span data-stu-id="93b8c-124">Specifies the deployment name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: dn

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93b8c-125">-ForceUpgrade</span><span class="sxs-lookup"><span data-stu-id="93b8c-125">-ForceUpgrade</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: f

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93b8c-126">-Start</span><span class="sxs-lookup"><span data-stu-id="93b8c-126">-Launch</span></span>
<span data-ttu-id="93b8c-127">Öffnet ein Browserfenster, in dem Sie die Anwendung anzeigen können, nachdem Sie bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="93b8c-127">Opens a browser window so you can view the application after it is deployed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93b8c-128">-Standort</span><span class="sxs-lookup"><span data-stu-id="93b8c-128">-Location</span></span>
<span data-ttu-id="93b8c-129">Der Bereich, in dem die Anwendung gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="93b8c-129">The region in which the application will be hosted.</span></span>
<span data-ttu-id="93b8c-130">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="93b8c-130">Possible values are:</span></span> 
  
- <span data-ttu-id="93b8c-131">Überall in Asien</span><span class="sxs-lookup"><span data-stu-id="93b8c-131">Anywhere Asia</span></span>
- <span data-ttu-id="93b8c-132">Überall in Europa</span><span class="sxs-lookup"><span data-stu-id="93b8c-132">Anywhere Europe</span></span>
- <span data-ttu-id="93b8c-133">Überall in den USA</span><span class="sxs-lookup"><span data-stu-id="93b8c-133">Anywhere US</span></span>
- <span data-ttu-id="93b8c-134">Ostasien</span><span class="sxs-lookup"><span data-stu-id="93b8c-134">East Asia</span></span>
- <span data-ttu-id="93b8c-135">East US</span><span class="sxs-lookup"><span data-stu-id="93b8c-135">East US</span></span>
- <span data-ttu-id="93b8c-136">Nord-Zentral-USA</span><span class="sxs-lookup"><span data-stu-id="93b8c-136">North Central US</span></span>
- <span data-ttu-id="93b8c-137">Nordeuropa</span><span class="sxs-lookup"><span data-stu-id="93b8c-137">North Europe</span></span>
- <span data-ttu-id="93b8c-138">Süd-Mittelamerika</span><span class="sxs-lookup"><span data-stu-id="93b8c-138">South Central US</span></span>
- <span data-ttu-id="93b8c-139">Südostasien</span><span class="sxs-lookup"><span data-stu-id="93b8c-139">Southeast Asia</span></span>
- <span data-ttu-id="93b8c-140">West Europa</span><span class="sxs-lookup"><span data-stu-id="93b8c-140">West Europe</span></span>
- <span data-ttu-id="93b8c-141">West-US</span><span class="sxs-lookup"><span data-stu-id="93b8c-141">West US</span></span>
 
<span data-ttu-id="93b8c-142">Wenn kein Standort angegeben ist, wird der im letzten Aufruf von **AzureServiceProject** angegebene Speicherort verwendet.</span><span class="sxs-lookup"><span data-stu-id="93b8c-142">If no Location is specified, the location specified in the last call to **Set-AzureServiceProject** will be used.</span></span> <span data-ttu-id="93b8c-143">Wenn kein Standort angegeben wurde, wird der Standort nach dem Zufallsprinzip aus den Speicherorten "North Central US" und "South Central US" ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="93b8c-143">If no Location was ever specified, the Location will be randomly chosen from 'North Central US' and 'South Central US' locations.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: l

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93b8c-144">-Paket</span><span class="sxs-lookup"><span data-stu-id="93b8c-144">-Package</span></span>
<span data-ttu-id="93b8c-145">Gibt die Paketdatei an, die bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="93b8c-145">Specifies the package file to deploy.</span></span>
<span data-ttu-id="93b8c-146">Geben Sie entweder eine lokale Datei mit der Dateinamenerweiterung cspkg oder einen URI mit einem BLOB an, das das Paket enthält.</span><span class="sxs-lookup"><span data-stu-id="93b8c-146">Specify either a local file that has the .cspkg file name extension or a URI of a blob that contains the package.</span></span>
<span data-ttu-id="93b8c-147">Wenn Sie diesen Parameter angeben, geben Sie den Parameter *ServiceName* nicht an.</span><span class="sxs-lookup"><span data-stu-id="93b8c-147">If you specify this parameter, do not specify the *ServiceName* parameter.</span></span>

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: sp

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93b8c-148">-Profil</span><span class="sxs-lookup"><span data-stu-id="93b8c-148">-Profile</span></span>
<span data-ttu-id="93b8c-149">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="93b8c-149">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="93b8c-150">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="93b8c-150">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="93b8c-151">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="93b8c-151">-ServiceName</span></span>
<span data-ttu-id="93b8c-152">Gibt den Namen an, der für den Dienst beim Veröffentlichen in Windows Azure verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="93b8c-152">Specifies the name to be used for the service when publishing to Windows Azure.</span></span>
<span data-ttu-id="93b8c-153">Der Name bestimmt einen Teil der Bezeichnung in der cloudapp.net-Unterdomäne, die verwendet wird, um den Dienst zu adressieren, wenn er in Windows Azure gehostet wird (also **Name**. cloudapp.net).</span><span class="sxs-lookup"><span data-stu-id="93b8c-153">The name determines part of the label in the cloudapp.net subdomain that is used to address the service when hosted in Windows Azure (that is, **name**.cloudapp.net).</span></span>
<span data-ttu-id="93b8c-154">Jeder beim Veröffentlichen des Diensts angegebene Name überschreibt den Namen, der beim Erstellen des Diensts angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="93b8c-154">Any name specified while publishing the service overrides the name given when the service was created.</span></span>
<span data-ttu-id="93b8c-155">(Siehe Cmdlet " **New-AzureServiceProject** ").</span><span class="sxs-lookup"><span data-stu-id="93b8c-155">(See the **New-AzureServiceProject** cmdlet).</span></span>

```yaml
Type: String
Parameter Sets: PublishFromServiceDefinition
Aliases: sv

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93b8c-156">-Slot</span><span class="sxs-lookup"><span data-stu-id="93b8c-156">-Slot</span></span>
<span data-ttu-id="93b8c-157">Der für diesen Dienst zu verwendende Bereitstellungs Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="93b8c-157">The deployment slot to be used for this service.</span></span>
<span data-ttu-id="93b8c-158">Mögliche Werte sind "Staging" und "Production".</span><span class="sxs-lookup"><span data-stu-id="93b8c-158">Possible values are 'Staging' and 'Production'.</span></span>
<span data-ttu-id="93b8c-159">Wenn kein Steckplatz angegeben ist, wird der im letzten Aufruf von Set-AzureDeploymentSlot angegebene Steckplatz verwendet.</span><span class="sxs-lookup"><span data-stu-id="93b8c-159">If no slot is specified, the slot provided in the last call to Set-AzureDeploymentSlot is used.</span></span>
<span data-ttu-id="93b8c-160">Wenn kein Steckplatz jemals angegeben wurde, wird der ' Production '-Slot verwendet.</span><span class="sxs-lookup"><span data-stu-id="93b8c-160">If no slot has ever been specified, the 'Production' slot is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: sl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93b8c-161">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="93b8c-161">-StorageAccountName</span></span>
<span data-ttu-id="93b8c-162">Gibt den Namen des Windows Azure-speicherkontos an, das beim Veröffentlichen des Diensts verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="93b8c-162">Specifies the Windows Azure storage account name to be used while publishing the service.</span></span>
<span data-ttu-id="93b8c-163">Dieser Wert wird erst verwendet, wenn der Dienst veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="93b8c-163">This value is not used until the service is published.</span></span>
<span data-ttu-id="93b8c-164">Wenn dieser Parameter nicht angegeben wird, wird der Wert aus dem letzten Befehl für **AzureServiceProject** abgerufen.</span><span class="sxs-lookup"><span data-stu-id="93b8c-164">When this parameter is not specified, the value is obtained from the last **Set-AzureServiceProject** command.</span></span>
<span data-ttu-id="93b8c-165">Wenn überhaupt kein Speicherkonto angegeben wurde, wird ein Speicherkonto verwendet, das dem Namen des Diensts entspricht.</span><span class="sxs-lookup"><span data-stu-id="93b8c-165">If no storage account was ever specified, a storage account matching the name of the service will be used.</span></span>
<span data-ttu-id="93b8c-166">Wenn kein solches Speicherkonto vorhanden ist, versucht das Cmdlet, eine neue zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="93b8c-166">If no such storage account exists, the cmdlet attempts to create a new one.</span></span>
<span data-ttu-id="93b8c-167">Der Versuch kann jedoch fehlschlagen, wenn ein Speicherkonto, das dem Dienstnamen entspricht, in einem anderen Abonnement vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="93b8c-167">However, the attempt may fail if a storage account matching the service name exists in another subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: st

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93b8c-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93b8c-168">CommonParameters</span></span>
<span data-ttu-id="93b8c-169">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93b8c-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93b8c-170">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93b8c-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93b8c-171">Eingaben</span><span class="sxs-lookup"><span data-stu-id="93b8c-171">INPUTS</span></span>

## <span data-ttu-id="93b8c-172">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="93b8c-172">OUTPUTS</span></span>

## <span data-ttu-id="93b8c-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="93b8c-173">NOTES</span></span>

## <span data-ttu-id="93b8c-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="93b8c-174">RELATED LINKS</span></span>

[<span data-ttu-id="93b8c-175">Enable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="93b8c-175">Enable-AzureServiceProjectRemoteDesktop</span></span>](./Enable-AzureServiceProjectRemoteDesktop.md)

[<span data-ttu-id="93b8c-176">Satz-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="93b8c-176">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)



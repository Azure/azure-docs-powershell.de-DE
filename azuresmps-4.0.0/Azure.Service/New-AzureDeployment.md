---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2BDB255A-EFB3-4580-BE95-187008DB208C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c21195f6d3ed938844717789f8a0df16f49fbd85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006135"
---
# <span data-ttu-id="b2642-101">New-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="b2642-101">New-AzureDeployment</span></span>

## <span data-ttu-id="b2642-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b2642-102">SYNOPSIS</span></span>
<span data-ttu-id="b2642-103">Erstellt eine Bereitstellung aus einem Dienst.</span><span class="sxs-lookup"><span data-stu-id="b2642-103">Creates a deployment from a service.</span></span>

## <span data-ttu-id="b2642-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2642-104">SYNTAX</span></span>

```
New-AzureDeployment [-ServiceName] <String> [-Package] <String> [-Configuration] <String> [-Slot] <String>
 [[-Label] <String>] [[-Name] <String>] [-DoNotStart] [-TreatWarningsAsError]
 [-ExtensionConfiguration <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b2642-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2642-105">DESCRIPTION</span></span>
<span data-ttu-id="b2642-106">Das Cmdlet **New-AzureDeployment** erstellt eine Azure-Bereitstellung von einem Dienst, der Webrollen und worker-Rollen umfasst.</span><span class="sxs-lookup"><span data-stu-id="b2642-106">The **New-AzureDeployment** cmdlet creates an Azure deployment from a service that comprises web roles and worker roles.</span></span>
<span data-ttu-id="b2642-107">Dieses Cmdlet erstellt eine Bereitstellung auf der Grundlage einer Paketdatei (cspkg) und einer Dienstkonfigurationsdatei (. cscfg).</span><span class="sxs-lookup"><span data-stu-id="b2642-107">This cmdlet creates a deployment based on a package file (.cspkg) and a service configuration file (.cscfg).</span></span>
<span data-ttu-id="b2642-108">Geben Sie einen Namen an, der innerhalb der Bereitstellungsumgebung eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="b2642-108">Specify a name that is unique within deployment environment.</span></span>

<span data-ttu-id="b2642-109">Verwenden Sie das Cmdlet **New-AzureVM** , um eine Bereitstellung basierend auf Azure Virtual Machines zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b2642-109">Use the **New-AzureVM** cmdlet to create a deployment based on Azure virtual machines.</span></span>

## <span data-ttu-id="b2642-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b2642-110">EXAMPLES</span></span>

### <span data-ttu-id="b2642-111">Beispiel 1: Erstellen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="b2642-111">Example 1: Create a deployment</span></span>
```
PS C:\> New-AzureDeployment -ServiceName "ContosoService" -Slot "Production" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -Label "ContosoDeployment"
```

<span data-ttu-id="b2642-112">Dieser Befehl erstellt eine Produktionsbereitstellung auf der Grundlage eines Pakets mit dem Namen "ContosoPackage. cspkg" und einer Konfiguration mit dem Namen ContosoConfiguration. cscfg.</span><span class="sxs-lookup"><span data-stu-id="b2642-112">This command creates a production deployment based on a package named ContosoPackage.cspkg and a configuration named ContosoConfiguration.cscfg.</span></span>
<span data-ttu-id="b2642-113">Der Befehl gibt eine Bezeichnung für die Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="b2642-113">The command specifies a label for the deployment.</span></span>
<span data-ttu-id="b2642-114">Es wird kein Name angegeben.</span><span class="sxs-lookup"><span data-stu-id="b2642-114">It does not specify a name.</span></span>
<span data-ttu-id="b2642-115">Mit diesem Cmdlet wird eine GUID als Name erstellt.</span><span class="sxs-lookup"><span data-stu-id="b2642-115">This cmdlet creates a GUID as the name.</span></span>

### <span data-ttu-id="b2642-116">Beispiel 2: Erstellen einer Bereitstellung auf der Grundlage einer Erweiterungskonfiguration</span><span class="sxs-lookup"><span data-stu-id="b2642-116">Example 2: Create a deployment based on an extension configuration</span></span>
```
PS C:\> New-AzureDeployment -ServiceName "ContosoService" -Slot "Production" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -ExtensionConfiguration "C:\packages\ContosoExtensionConfig.cscfg"
```

<span data-ttu-id="b2642-117">Dieser Befehl erstellt eine Produktionsbereitstellung auf der Grundlage eines Pakets und einer Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b2642-117">This command creates a production deployment based on a package and configuration.</span></span>
<span data-ttu-id="b2642-118">Der Befehl gibt eine Erweiterungskonfiguration mit dem Namen "ContosoExtensionConfig. cscfg" an.</span><span class="sxs-lookup"><span data-stu-id="b2642-118">The command specifies an extension configuration named ContosoExtensionConfig.cscfg.</span></span>
<span data-ttu-id="b2642-119">Dieses Cmdlet erstellt GUIDs als Namen und Beschriftung.</span><span class="sxs-lookup"><span data-stu-id="b2642-119">This cmdlet creates GUIDs as the name and the label.</span></span>

## <span data-ttu-id="b2642-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2642-120">PARAMETERS</span></span>

### <span data-ttu-id="b2642-121">-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="b2642-121">-Configuration</span></span>
<span data-ttu-id="b2642-122">Gibt den vollständigen Pfad einer Dienst Konfigurationsdatei an.</span><span class="sxs-lookup"><span data-stu-id="b2642-122">Specifies the full path of a service configuration file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2642-123">-DoNotStart</span><span class="sxs-lookup"><span data-stu-id="b2642-123">-DoNotStart</span></span>
<span data-ttu-id="b2642-124">Gibt an, dass dieses Cmdlet die Bereitstellung nicht startet.</span><span class="sxs-lookup"><span data-stu-id="b2642-124">Specifies that this cmdlet does not start the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2642-125">-ExtensionConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2642-125">-ExtensionConfiguration</span></span>
<span data-ttu-id="b2642-126">Gibt ein Array von Erweiterungs Konfigurationsobjekten an.</span><span class="sxs-lookup"><span data-stu-id="b2642-126">Specifies an array of extension configuration objects.</span></span>

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2642-127">-Information</span><span class="sxs-lookup"><span data-stu-id="b2642-127">-InformationAction</span></span>
<span data-ttu-id="b2642-128">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="b2642-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b2642-129">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b2642-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b2642-130">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="b2642-130">Continue</span></span>
- <span data-ttu-id="b2642-131">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="b2642-131">Ignore</span></span>
- <span data-ttu-id="b2642-132">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="b2642-132">Inquire</span></span>
- <span data-ttu-id="b2642-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b2642-133">SilentlyContinue</span></span>
- <span data-ttu-id="b2642-134">Beenden</span><span class="sxs-lookup"><span data-stu-id="b2642-134">Stop</span></span>
- <span data-ttu-id="b2642-135">Anhalten</span><span class="sxs-lookup"><span data-stu-id="b2642-135">Suspend</span></span>

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

### <span data-ttu-id="b2642-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b2642-136">-InformationVariable</span></span>
<span data-ttu-id="b2642-137">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="b2642-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b2642-138">-Label</span><span class="sxs-lookup"><span data-stu-id="b2642-138">-Label</span></span>
<span data-ttu-id="b2642-139">Gibt einen Etikettennamen für die Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="b2642-139">Specifies a label name for the deployment.</span></span>
<span data-ttu-id="b2642-140">Wenn Sie keine Beschriftung angeben, verwendet dieses Cmdlet eine GUID.</span><span class="sxs-lookup"><span data-stu-id="b2642-140">If you do not specify a label, this cmdlet uses a GUID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2642-141">-Name</span><span class="sxs-lookup"><span data-stu-id="b2642-141">-Name</span></span>
<span data-ttu-id="b2642-142">Gibt einen Bereitstellungsnamen an.</span><span class="sxs-lookup"><span data-stu-id="b2642-142">Specifies a deployment name.</span></span>
<span data-ttu-id="b2642-143">Wenn Sie keinen Namen angeben, verwendet dieses Cmdlet eine GUID.</span><span class="sxs-lookup"><span data-stu-id="b2642-143">If you do not specify a name, this cmdlet uses a GUID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2642-144">-Paket</span><span class="sxs-lookup"><span data-stu-id="b2642-144">-Package</span></span>
<span data-ttu-id="b2642-145">Gibt den Pfad oder URI einer cspkg-Datei im Speicher innerhalb desselben Abonnements oder Projekts an.</span><span class="sxs-lookup"><span data-stu-id="b2642-145">Specifies the path or URI of a .cspkg file in storage within the same subscription or project.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2642-146">-Profil</span><span class="sxs-lookup"><span data-stu-id="b2642-146">-Profile</span></span>
<span data-ttu-id="b2642-147">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="b2642-147">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b2642-148">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="b2642-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b2642-149">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b2642-149">-ServiceName</span></span>
<span data-ttu-id="b2642-150">Gibt den Namen des Azure-Diensts für die Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="b2642-150">Specifies the name of the Azure service for the deployment.</span></span>

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

### <span data-ttu-id="b2642-151">-Slot</span><span class="sxs-lookup"><span data-stu-id="b2642-151">-Slot</span></span>
<span data-ttu-id="b2642-152">Gibt die Umgebung an, in der dieses Cmdlet die Bereitstellung erstellt.</span><span class="sxs-lookup"><span data-stu-id="b2642-152">Specifies the environment where this cmdlet creates the deployment.</span></span>
<span data-ttu-id="b2642-153">Gültige Werte sind: Staging und Production.</span><span class="sxs-lookup"><span data-stu-id="b2642-153">Valid values are: Staging and Production.</span></span>
<span data-ttu-id="b2642-154">Der Standardwert ist Production.</span><span class="sxs-lookup"><span data-stu-id="b2642-154">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2642-155">-TreatWarningsAsError</span><span class="sxs-lookup"><span data-stu-id="b2642-155">-TreatWarningsAsError</span></span>
<span data-ttu-id="b2642-156">Gibt an, dass Warnmeldungen Fehler sind.</span><span class="sxs-lookup"><span data-stu-id="b2642-156">Specifies that warning messages are errors.</span></span>
<span data-ttu-id="b2642-157">Wenn Sie diesen Parameter angeben, führt eine Warnmeldung dazu, dass die Bereitstellung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="b2642-157">If you specify this parameter, a warning message causes the deployment to fail.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2642-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2642-158">CommonParameters</span></span>
<span data-ttu-id="b2642-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2642-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2642-160">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2642-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2642-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b2642-161">INPUTS</span></span>

## <span data-ttu-id="b2642-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b2642-162">OUTPUTS</span></span>

## <span data-ttu-id="b2642-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="b2642-163">NOTES</span></span>

## <span data-ttu-id="b2642-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b2642-164">RELATED LINKS</span></span>

[<span data-ttu-id="b2642-165">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="b2642-165">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="b2642-166">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="b2642-166">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="b2642-167">Verschieben-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="b2642-167">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="b2642-168">Neu – AzureVM</span><span class="sxs-lookup"><span data-stu-id="b2642-168">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="b2642-169">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="b2642-169">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="b2642-170">Satz-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="b2642-170">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 2228eb7562ed7a0ffa1c0098086c085985e45fee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996195"
---
# <span data-ttu-id="edbca-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="edbca-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="edbca-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="edbca-102">SYNOPSIS</span></span>
<span data-ttu-id="edbca-103">Erstellt einen Azure Web App-Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="edbca-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="edbca-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="edbca-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edbca-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="edbca-105">DESCRIPTION</span></span>
<span data-ttu-id="edbca-106">Mit dem Cmdlet **New-AzWebAppSlot** wird ein Azure Web App-Slot in einer bestimmten Ressourcengruppe erstellt, die den angegebenen app-Service Plan und das Rechenzentrum verwendet.</span><span class="sxs-lookup"><span data-stu-id="edbca-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="edbca-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="edbca-107">EXAMPLES</span></span>

### <span data-ttu-id="edbca-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="edbca-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="edbca-109">Dieser Befehl erstellt einen Steckplatz mit dem Namen Slot001 unter einem vorhandenen Web-App-Namen ContosoSite in der vorhandenen Ressourcengruppe Default-Web-westus in Rechenzentrum West USA.</span><span class="sxs-lookup"><span data-stu-id="edbca-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="edbca-110">Der Befehl verwendet einen vorhandenen APP-Service Plan mit dem Namen ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="edbca-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="edbca-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="edbca-111">PARAMETERS</span></span>

### <span data-ttu-id="edbca-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="edbca-112">-AppServicePlan</span></span>
<span data-ttu-id="edbca-113">Name des App-Service Plans oder App-Service Plan-ID. Wenn sich der Slot-und App-Service Plan in verschiedenen Ressourcengruppen befindet, verwenden Sie die ID anstelle des Namens.</span><span class="sxs-lookup"><span data-stu-id="edbca-113">App Service Plan Name or App Service Plan Id. If the Slot and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="edbca-114">Die APP-Service Plan-ID kann mit folgendem abgerufen werden: $ASP = Get-AzAppServicePlan-ResourceGroup myRG-Name Web$ASP. ID gibt die ID des App-Service Plans zurück.</span><span class="sxs-lookup"><span data-stu-id="edbca-114">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edbca-115">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="edbca-115">-AppSettingsOverrides</span></span>
<span data-ttu-id="edbca-116">App-Einstellungen setzen Hashtable außer Kraft</span><span class="sxs-lookup"><span data-stu-id="edbca-116">App Settings Overrides Hashtable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edbca-117">-AseName</span><span class="sxs-lookup"><span data-stu-id="edbca-117">-AseName</span></span>
<span data-ttu-id="edbca-118">Name der APP-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="edbca-118">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edbca-119">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edbca-119">-AseResourceGroupName</span></span>
<span data-ttu-id="edbca-120">Ressourcengruppen Name der APP-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="edbca-120">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edbca-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="edbca-121">-AsJob</span></span>
<span data-ttu-id="edbca-122">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="edbca-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="edbca-123">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="edbca-123">-ContainerImageName</span></span>
<span data-ttu-id="edbca-124">Name des Container Bilds und optionales Tag, beispielsweise (Bild: Tag)</span><span class="sxs-lookup"><span data-stu-id="edbca-124">Container Image Name and optional tag, for example (image:tag)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edbca-125">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="edbca-125">-ContainerRegistryPassword</span></span>
<span data-ttu-id="edbca-126">Registrierungskennwort für private Container</span><span class="sxs-lookup"><span data-stu-id="edbca-126">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edbca-127">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="edbca-127">-ContainerRegistryUrl</span></span>
<span data-ttu-id="edbca-128">URL des Registrierungsservers für private Container</span><span class="sxs-lookup"><span data-stu-id="edbca-128">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edbca-129">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="edbca-129">-ContainerRegistryUser</span></span>
<span data-ttu-id="edbca-130">Benutzername für private Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="edbca-130">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edbca-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edbca-131">-DefaultProfile</span></span>
<span data-ttu-id="edbca-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="edbca-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edbca-133">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="edbca-133">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="edbca-134">Aktiviert/deaktiviert die Container-fortlaufende Bereitstellung webhook</span><span class="sxs-lookup"><span data-stu-id="edbca-134">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="edbca-135">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="edbca-135">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="edbca-136">Option "benutzerdefinierte hostnames ignorieren"</span><span class="sxs-lookup"><span data-stu-id="edbca-136">Ignore Custom HostNames Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edbca-137">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="edbca-137">-IgnoreSourceControl</span></span>
<span data-ttu-id="edbca-138">Option "Quellcodeverwaltung ignorieren"</span><span class="sxs-lookup"><span data-stu-id="edbca-138">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edbca-139">-Name</span><span class="sxs-lookup"><span data-stu-id="edbca-139">-Name</span></span>
<span data-ttu-id="edbca-140">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="edbca-140">Webapp Name</span></span>

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

### <span data-ttu-id="edbca-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edbca-141">-ResourceGroupName</span></span>
<span data-ttu-id="edbca-142">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="edbca-142">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edbca-143">-Slot</span><span class="sxs-lookup"><span data-stu-id="edbca-143">-Slot</span></span>
<span data-ttu-id="edbca-144">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="edbca-144">Webapp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edbca-145">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="edbca-145">-SourceWebApp</span></span>
<span data-ttu-id="edbca-146">Quell-Webobjekt</span><span class="sxs-lookup"><span data-stu-id="edbca-146">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="edbca-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edbca-147">CommonParameters</span></span>
<span data-ttu-id="edbca-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edbca-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edbca-149">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edbca-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edbca-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="edbca-150">INPUTS</span></span>

### <span data-ttu-id="edbca-151">System. String</span><span class="sxs-lookup"><span data-stu-id="edbca-151">System.String</span></span>

### <span data-ttu-id="edbca-152">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="edbca-152">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="edbca-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="edbca-153">OUTPUTS</span></span>

### <span data-ttu-id="edbca-154">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="edbca-154">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="edbca-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="edbca-155">NOTES</span></span>

## <span data-ttu-id="edbca-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="edbca-156">RELATED LINKS</span></span>

[<span data-ttu-id="edbca-157">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="edbca-157">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="edbca-158">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="edbca-158">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="edbca-159">Neustart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="edbca-159">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="edbca-160">Satz-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="edbca-160">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="edbca-161">Anfang-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="edbca-161">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="edbca-162">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="edbca-162">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="edbca-163">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="edbca-163">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="edbca-164">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="edbca-164">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

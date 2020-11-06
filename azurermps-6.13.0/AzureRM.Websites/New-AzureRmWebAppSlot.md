---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
ms.openlocfilehash: 6c7fbd4512bfac7a369f21f85803653c6f7c9628
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502793"
---
# <span data-ttu-id="c590b-101">New-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c590b-101">New-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="c590b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c590b-102">SYNOPSIS</span></span>
<span data-ttu-id="c590b-103">Erstellt einen Azure Web App-Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="c590b-103">Creates an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c590b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c590b-104">SYNTAX</span></span>

```
New-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c590b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c590b-105">DESCRIPTION</span></span>
<span data-ttu-id="c590b-106">Mit dem Cmdlet **New-AzureRmWebAppSlot** wird ein Azure Web App-Slot in einer bestimmten Ressourcengruppe erstellt, die den angegebenen app-Service Plan und das Rechenzentrum verwendet.</span><span class="sxs-lookup"><span data-stu-id="c590b-106">The **New-AzureRmWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="c590b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c590b-107">EXAMPLES</span></span>

### <span data-ttu-id="c590b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c590b-108">Example 1</span></span>
```
PS C:\> New-AzureRmWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="c590b-109">Dieser Befehl erstellt einen Steckplatz mit dem Namen Slot001 unter einem vorhandenen Web-App-Namen ContosoSite in der vorhandenen Ressourcengruppe Default-Web-westus in Rechenzentrum West USA.</span><span class="sxs-lookup"><span data-stu-id="c590b-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="c590b-110">Der Befehl verwendet einen vorhandenen APP-Service Plan mit dem Namen ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="c590b-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="c590b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c590b-111">PARAMETERS</span></span>

### <span data-ttu-id="c590b-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c590b-112">-AppServicePlan</span></span>
<span data-ttu-id="c590b-113">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="c590b-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="c590b-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="c590b-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="c590b-115">App-Einstellungen setzen Hashtable außer Kraft</span><span class="sxs-lookup"><span data-stu-id="c590b-115">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="c590b-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="c590b-116">-AseName</span></span>
<span data-ttu-id="c590b-117">Name der APP-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="c590b-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="c590b-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c590b-118">-AseResourceGroupName</span></span>
<span data-ttu-id="c590b-119">Ressourcengruppen Name der APP-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="c590b-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="c590b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c590b-120">-AsJob</span></span>
<span data-ttu-id="c590b-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c590b-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c590b-122">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="c590b-122">-ContainerImageName</span></span>
<span data-ttu-id="c590b-123">Name des Container Bilds und optionales Tag, beispielsweise (Bild: Tag)</span><span class="sxs-lookup"><span data-stu-id="c590b-123">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="c590b-124">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="c590b-124">-ContainerRegistryPassword</span></span>
<span data-ttu-id="c590b-125">Registrierungskennwort für private Container</span><span class="sxs-lookup"><span data-stu-id="c590b-125">Private Container Registry Password</span></span>

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

### <span data-ttu-id="c590b-126">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="c590b-126">-ContainerRegistryUrl</span></span>
<span data-ttu-id="c590b-127">URL des Registrierungsservers für private Container</span><span class="sxs-lookup"><span data-stu-id="c590b-127">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="c590b-128">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="c590b-128">-ContainerRegistryUser</span></span>
<span data-ttu-id="c590b-129">Benutzername für private Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="c590b-129">Private Container Registry Username</span></span>

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

### <span data-ttu-id="c590b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c590b-130">-DefaultProfile</span></span>
<span data-ttu-id="c590b-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c590b-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c590b-132">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="c590b-132">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="c590b-133">Aktiviert/deaktiviert die Container-fortlaufende Bereitstellung webhook</span><span class="sxs-lookup"><span data-stu-id="c590b-133">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="c590b-134">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="c590b-134">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="c590b-135">Option "benutzerdefinierte hostnames ignorieren"</span><span class="sxs-lookup"><span data-stu-id="c590b-135">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="c590b-136">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="c590b-136">-IgnoreSourceControl</span></span>
<span data-ttu-id="c590b-137">Option "Quellcodeverwaltung ignorieren"</span><span class="sxs-lookup"><span data-stu-id="c590b-137">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="c590b-138">-Name</span><span class="sxs-lookup"><span data-stu-id="c590b-138">-Name</span></span>
<span data-ttu-id="c590b-139">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="c590b-139">Webapp Name</span></span>

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

### <span data-ttu-id="c590b-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c590b-140">-ResourceGroupName</span></span>
<span data-ttu-id="c590b-141">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="c590b-141">Resource Group Name</span></span>

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

### <span data-ttu-id="c590b-142">-Slot</span><span class="sxs-lookup"><span data-stu-id="c590b-142">-Slot</span></span>
<span data-ttu-id="c590b-143">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="c590b-143">Webapp Slot Name</span></span>

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

### <span data-ttu-id="c590b-144">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="c590b-144">-SourceWebApp</span></span>
<span data-ttu-id="c590b-145">Quell-Webobjekt</span><span class="sxs-lookup"><span data-stu-id="c590b-145">Source WebApp Object</span></span>

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

### <span data-ttu-id="c590b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c590b-146">CommonParameters</span></span>
<span data-ttu-id="c590b-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c590b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c590b-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c590b-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c590b-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c590b-149">INPUTS</span></span>

### <span data-ttu-id="c590b-150">System. String</span><span class="sxs-lookup"><span data-stu-id="c590b-150">System.String</span></span>

### <span data-ttu-id="c590b-151">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="c590b-151">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="c590b-152">Parameter: SourceWebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c590b-152">Parameters: SourceWebApp (ByValue)</span></span>

## <span data-ttu-id="c590b-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c590b-153">OUTPUTS</span></span>

### <span data-ttu-id="c590b-154">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="c590b-154">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="c590b-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="c590b-155">NOTES</span></span>

## <span data-ttu-id="c590b-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c590b-156">RELATED LINKS</span></span>

[<span data-ttu-id="c590b-157">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c590b-157">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="c590b-158">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c590b-158">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="c590b-159">Neustart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c590b-159">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="c590b-160">Satz-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c590b-160">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="c590b-161">Anfang-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c590b-161">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="c590b-162">Stopp-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c590b-162">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="c590b-163">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c590b-163">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="c590b-164">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c590b-164">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

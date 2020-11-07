---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 941de31e1733bd591507176216e30f9e1510f706
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658531"
---
# <span data-ttu-id="8838e-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8838e-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="8838e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8838e-102">SYNOPSIS</span></span>
<span data-ttu-id="8838e-103">Erstellt einen Azure Web App-Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="8838e-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="8838e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8838e-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8838e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8838e-105">DESCRIPTION</span></span>
<span data-ttu-id="8838e-106">Mit dem Cmdlet **New-AzWebAppSlot** wird ein Azure Web App-Slot in einer bestimmten Ressourcengruppe erstellt, die den angegebenen app-Service Plan und das Rechenzentrum verwendet.</span><span class="sxs-lookup"><span data-stu-id="8838e-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="8838e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8838e-107">EXAMPLES</span></span>

### <span data-ttu-id="8838e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8838e-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="8838e-109">Dieser Befehl erstellt einen Steckplatz mit dem Namen Slot001 unter einem vorhandenen Web-App-Namen ContosoSite in der vorhandenen Ressourcengruppe Default-Web-westus in Rechenzentrum West USA.</span><span class="sxs-lookup"><span data-stu-id="8838e-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="8838e-110">Der Befehl verwendet einen vorhandenen APP-Service Plan mit dem Namen ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="8838e-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="8838e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="8838e-111">PARAMETERS</span></span>

### <span data-ttu-id="8838e-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8838e-112">-AppServicePlan</span></span>
<span data-ttu-id="8838e-113">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="8838e-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="8838e-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="8838e-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="8838e-115">App-Einstellungen setzen Hashtable außer Kraft</span><span class="sxs-lookup"><span data-stu-id="8838e-115">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="8838e-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="8838e-116">-AseName</span></span>
<span data-ttu-id="8838e-117">Name der APP-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="8838e-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="8838e-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8838e-118">-AseResourceGroupName</span></span>
<span data-ttu-id="8838e-119">Ressourcengruppen Name der APP-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="8838e-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="8838e-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8838e-120">-AsJob</span></span>
<span data-ttu-id="8838e-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8838e-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8838e-122">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="8838e-122">-ContainerImageName</span></span>
<span data-ttu-id="8838e-123">Name des Container Bilds und optionales Tag, beispielsweise (Bild: Tag)</span><span class="sxs-lookup"><span data-stu-id="8838e-123">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="8838e-124">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="8838e-124">-ContainerRegistryPassword</span></span>
<span data-ttu-id="8838e-125">Registrierungskennwort für private Container</span><span class="sxs-lookup"><span data-stu-id="8838e-125">Private Container Registry Password</span></span>

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

### <span data-ttu-id="8838e-126">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="8838e-126">-ContainerRegistryUrl</span></span>
<span data-ttu-id="8838e-127">URL des Registrierungsservers für private Container</span><span class="sxs-lookup"><span data-stu-id="8838e-127">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="8838e-128">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="8838e-128">-ContainerRegistryUser</span></span>
<span data-ttu-id="8838e-129">Benutzername für private Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="8838e-129">Private Container Registry Username</span></span>

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

### <span data-ttu-id="8838e-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8838e-130">-DefaultProfile</span></span>
<span data-ttu-id="8838e-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8838e-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8838e-132">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="8838e-132">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="8838e-133">Aktiviert/deaktiviert die Container-fortlaufende Bereitstellung webhook</span><span class="sxs-lookup"><span data-stu-id="8838e-133">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="8838e-134">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="8838e-134">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="8838e-135">Option "benutzerdefinierte hostnames ignorieren"</span><span class="sxs-lookup"><span data-stu-id="8838e-135">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="8838e-136">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="8838e-136">-IgnoreSourceControl</span></span>
<span data-ttu-id="8838e-137">Option "Quellcodeverwaltung ignorieren"</span><span class="sxs-lookup"><span data-stu-id="8838e-137">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="8838e-138">-Name</span><span class="sxs-lookup"><span data-stu-id="8838e-138">-Name</span></span>
<span data-ttu-id="8838e-139">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="8838e-139">Webapp Name</span></span>

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

### <span data-ttu-id="8838e-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8838e-140">-ResourceGroupName</span></span>
<span data-ttu-id="8838e-141">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="8838e-141">Resource Group Name</span></span>

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

### <span data-ttu-id="8838e-142">-Slot</span><span class="sxs-lookup"><span data-stu-id="8838e-142">-Slot</span></span>
<span data-ttu-id="8838e-143">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="8838e-143">Webapp Slot Name</span></span>

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

### <span data-ttu-id="8838e-144">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="8838e-144">-SourceWebApp</span></span>
<span data-ttu-id="8838e-145">Quell-Webobjekt</span><span class="sxs-lookup"><span data-stu-id="8838e-145">Source WebApp Object</span></span>

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

### <span data-ttu-id="8838e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8838e-146">CommonParameters</span></span>
<span data-ttu-id="8838e-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8838e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8838e-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8838e-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8838e-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8838e-149">INPUTS</span></span>

### <span data-ttu-id="8838e-150">System. String</span><span class="sxs-lookup"><span data-stu-id="8838e-150">System.String</span></span>

### <span data-ttu-id="8838e-151">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="8838e-151">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8838e-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8838e-152">OUTPUTS</span></span>

### <span data-ttu-id="8838e-153">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="8838e-153">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8838e-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="8838e-154">NOTES</span></span>

## <span data-ttu-id="8838e-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8838e-155">RELATED LINKS</span></span>

[<span data-ttu-id="8838e-156">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8838e-156">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="8838e-157">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8838e-157">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="8838e-158">Neustart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8838e-158">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="8838e-159">Satz-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8838e-159">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="8838e-160">Anfang-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8838e-160">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="8838e-161">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8838e-161">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="8838e-162">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8838e-162">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="8838e-163">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8838e-163">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

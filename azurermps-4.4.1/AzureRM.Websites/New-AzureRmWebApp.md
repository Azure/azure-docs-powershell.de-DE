---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
ms.openlocfilehash: 4948de891815345efdc0b3f4ec39fb1874e510b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504685"
---
# <span data-ttu-id="faf4d-101">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="faf4d-101">New-AzureRmWebApp</span></span>

## <span data-ttu-id="faf4d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="faf4d-102">SYNOPSIS</span></span>
<span data-ttu-id="faf4d-103">Erstellt eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="faf4d-103">Creates an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="faf4d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="faf4d-104">SYNTAX</span></span>

### <span data-ttu-id="faf4d-105">S1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="faf4d-105">S1 (Default)</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [[-TrafficManagerProfileId] <String>]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="faf4d-106">S2</span><span class="sxs-lookup"><span data-stu-id="faf4d-106">S2</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [[-TrafficManagerProfileName] <String>]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="faf4d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="faf4d-107">DESCRIPTION</span></span>
<span data-ttu-id="faf4d-108">Mit dem Cmdlet **New-AzureRmWebApp** wird eine Azure Web App in einer bestimmten Ressourcengruppe erstellt, die den angegebenen app-Service Plan und das Rechenzentrum verwendet.</span><span class="sxs-lookup"><span data-stu-id="faf4d-108">The **New-AzureRmWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="faf4d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="faf4d-109">EXAMPLES</span></span>

### <span data-ttu-id="faf4d-110">Beispiel 1: Erstellen einer Web-App</span><span class="sxs-lookup"><span data-stu-id="faf4d-110">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzureRmWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="faf4d-111">Mit diesem Befehl wird eine Azure Web App mit dem Namen ContosoSite in der vorhandenen Ressourcengruppe Default-Web-westus in Rechenzentrum West US erstellt.</span><span class="sxs-lookup"><span data-stu-id="faf4d-111">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="faf4d-112">Der Befehl verwendet einen vorhandenen APP-Service Plan mit dem Namen ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="faf4d-112">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="faf4d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="faf4d-113">PARAMETERS</span></span>

### <span data-ttu-id="faf4d-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="faf4d-114">-AppServicePlan</span></span>
<span data-ttu-id="faf4d-115">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="faf4d-115">App Service Plan Name</span></span>

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

### <span data-ttu-id="faf4d-116">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="faf4d-116">-AppSettingsOverrides</span></span>
<span data-ttu-id="faf4d-117">App-Einstellungen setzen Hashtable außer Kraft</span><span class="sxs-lookup"><span data-stu-id="faf4d-117">App Settings Overrides HashTable</span></span>

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

### <span data-ttu-id="faf4d-118">-AseName</span><span class="sxs-lookup"><span data-stu-id="faf4d-118">-AseName</span></span>
<span data-ttu-id="faf4d-119">Name der APP-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="faf4d-119">App Service Environment Name</span></span>

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

### <span data-ttu-id="faf4d-120">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faf4d-120">-AseResourceGroupName</span></span>
<span data-ttu-id="faf4d-121">Ressourcengruppen Name der APP-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="faf4d-121">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="faf4d-122">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="faf4d-122">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="faf4d-123">Option "benutzerdefinierte Hostnamen ignorieren"</span><span class="sxs-lookup"><span data-stu-id="faf4d-123">Ignore Custom Host Names Option</span></span>

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

### <span data-ttu-id="faf4d-124">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="faf4d-124">-IgnoreSourceControl</span></span>
<span data-ttu-id="faf4d-125">Option "Quellcodeverwaltung ignorieren"</span><span class="sxs-lookup"><span data-stu-id="faf4d-125">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="faf4d-126">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="faf4d-126">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="faf4d-127">Option "Quell-Webspiel Steckplätze einbeziehen"</span><span class="sxs-lookup"><span data-stu-id="faf4d-127">Include Source WebApp Slots Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf4d-128">-Standort</span><span class="sxs-lookup"><span data-stu-id="faf4d-128">-Location</span></span>
<span data-ttu-id="faf4d-129">Lage</span><span class="sxs-lookup"><span data-stu-id="faf4d-129">Location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf4d-130">-Name</span><span class="sxs-lookup"><span data-stu-id="faf4d-130">-Name</span></span>
<span data-ttu-id="faf4d-131">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="faf4d-131">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf4d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faf4d-132">-ResourceGroupName</span></span>
<span data-ttu-id="faf4d-133">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="faf4d-133">Resource Group Name</span></span>

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

### <span data-ttu-id="faf4d-134">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="faf4d-134">-SourceWebApp</span></span>
<span data-ttu-id="faf4d-135">Quell-Webobjekt</span><span class="sxs-lookup"><span data-stu-id="faf4d-135">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="faf4d-136">-TrafficManagerProfileId</span><span class="sxs-lookup"><span data-stu-id="faf4d-136">-TrafficManagerProfileId</span></span>
<span data-ttu-id="faf4d-137">Profil-ID des Datenverkehrs-Managers</span><span class="sxs-lookup"><span data-stu-id="faf4d-137">Traffic Manager Profile Id</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf4d-138">-TrafficManagerProfileName</span><span class="sxs-lookup"><span data-stu-id="faf4d-138">-TrafficManagerProfileName</span></span>
<span data-ttu-id="faf4d-139">Profil Name des Datenverkehrs-Managers</span><span class="sxs-lookup"><span data-stu-id="faf4d-139">Traffic Manager Profile Name</span></span>

```yaml
Type: System.String
Parameter Sets: S2
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf4d-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faf4d-140">-DefaultProfile</span></span>
<span data-ttu-id="faf4d-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="faf4d-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="faf4d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faf4d-142">CommonParameters</span></span>
<span data-ttu-id="faf4d-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faf4d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faf4d-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faf4d-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faf4d-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="faf4d-145">INPUTS</span></span>

### <span data-ttu-id="faf4d-146">Website</span><span class="sxs-lookup"><span data-stu-id="faf4d-146">Site</span></span>
<span data-ttu-id="faf4d-147">Der Parameter "SourceWebApp" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="faf4d-147">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="faf4d-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="faf4d-148">OUTPUTS</span></span>

## <span data-ttu-id="faf4d-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="faf4d-149">NOTES</span></span>

## <span data-ttu-id="faf4d-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="faf4d-150">RELATED LINKS</span></span>

[<span data-ttu-id="faf4d-151">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="faf4d-151">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="faf4d-152">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="faf4d-152">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="faf4d-153">Neustart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="faf4d-153">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="faf4d-154">Anfang-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="faf4d-154">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="faf4d-155">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="faf4d-155">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)



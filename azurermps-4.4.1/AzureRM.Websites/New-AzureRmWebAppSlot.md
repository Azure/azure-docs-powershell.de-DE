---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
ms.openlocfilehash: 3e886803ff608522bd2d563dd9b6cd6effcfe074
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504669"
---
# <span data-ttu-id="bf556-101">New-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bf556-101">New-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="bf556-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bf556-102">SYNOPSIS</span></span>
<span data-ttu-id="bf556-103">Erstellt einen Azure Web App-Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="bf556-103">Creates an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf556-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf556-104">SYNTAX</span></span>

```
New-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf556-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf556-105">DESCRIPTION</span></span>
<span data-ttu-id="bf556-106">Mit dem Cmdlet **New-AzureRmWebAppSlot** wird ein Azure Web App-Slot in einer bestimmten Ressourcengruppe erstellt, die den angegebenen app-Service Plan und das Rechenzentrum verwendet.</span><span class="sxs-lookup"><span data-stu-id="bf556-106">The **New-AzureRmWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="bf556-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bf556-107">EXAMPLES</span></span>

### <span data-ttu-id="bf556-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bf556-108">Example 1</span></span>
```
PS C:\> New-AzureRmWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="bf556-109">Dieser Befehl erstellt einen Steckplatz mit dem Namen Slot001 unter einem vorhandenen Web-App-Namen ContosoSite in der vorhandenen Ressourcengruppe Default-Web-westus in Rechenzentrum West USA.</span><span class="sxs-lookup"><span data-stu-id="bf556-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="bf556-110">Der Befehl verwendet einen vorhandenen APP-Service Plan mit dem Namen ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="bf556-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="bf556-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf556-111">PARAMETERS</span></span>

### <span data-ttu-id="bf556-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bf556-112">-AppServicePlan</span></span>
<span data-ttu-id="bf556-113">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="bf556-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="bf556-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="bf556-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="bf556-115">App-Einstellungen setzen Hashtable außer Kraft</span><span class="sxs-lookup"><span data-stu-id="bf556-115">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="bf556-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="bf556-116">-AseName</span></span>
<span data-ttu-id="bf556-117">Name der APP-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="bf556-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="bf556-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf556-118">-AseResourceGroupName</span></span>
<span data-ttu-id="bf556-119">Ressourcengruppen Name der APP-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="bf556-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="bf556-120">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="bf556-120">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="bf556-121">Option "benutzerdefinierte hostnames ignorieren"</span><span class="sxs-lookup"><span data-stu-id="bf556-121">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="bf556-122">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="bf556-122">-IgnoreSourceControl</span></span>
<span data-ttu-id="bf556-123">Option "Quellcodeverwaltung ignorieren"</span><span class="sxs-lookup"><span data-stu-id="bf556-123">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="bf556-124">-Name</span><span class="sxs-lookup"><span data-stu-id="bf556-124">-Name</span></span>
<span data-ttu-id="bf556-125">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="bf556-125">Webapp Name</span></span>

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

### <span data-ttu-id="bf556-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf556-126">-ResourceGroupName</span></span>
<span data-ttu-id="bf556-127">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="bf556-127">Resource Group Name</span></span>

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

### <span data-ttu-id="bf556-128">-Slot</span><span class="sxs-lookup"><span data-stu-id="bf556-128">-Slot</span></span>
<span data-ttu-id="bf556-129">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="bf556-129">Webapp Slot Name</span></span>

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

### <span data-ttu-id="bf556-130">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="bf556-130">-SourceWebApp</span></span>
<span data-ttu-id="bf556-131">Quell-Webobjekt</span><span class="sxs-lookup"><span data-stu-id="bf556-131">Source WebApp Object</span></span>

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

### <span data-ttu-id="bf556-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf556-132">-DefaultProfile</span></span>
<span data-ttu-id="bf556-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bf556-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf556-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf556-134">CommonParameters</span></span>
<span data-ttu-id="bf556-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf556-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf556-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf556-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf556-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bf556-137">INPUTS</span></span>

### <span data-ttu-id="bf556-138">Website</span><span class="sxs-lookup"><span data-stu-id="bf556-138">Site</span></span>
<span data-ttu-id="bf556-139">Der Parameter "SourceWebApp" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="bf556-139">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="bf556-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bf556-140">OUTPUTS</span></span>

## <span data-ttu-id="bf556-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="bf556-141">NOTES</span></span>

## <span data-ttu-id="bf556-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bf556-142">RELATED LINKS</span></span>

[<span data-ttu-id="bf556-143">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bf556-143">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="bf556-144">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bf556-144">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="bf556-145">Neustart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bf556-145">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="bf556-146">Satz-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bf556-146">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="bf556-147">Anfang-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bf556-147">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="bf556-148">Stopp-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bf556-148">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="bf556-149">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bf556-149">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="bf556-150">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="bf556-150">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

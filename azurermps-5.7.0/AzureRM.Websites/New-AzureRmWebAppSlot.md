---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
ms.openlocfilehash: a3ae7f879827b7b260e60f0d3e0aa70e5a6ab533
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480722"
---
# <span data-ttu-id="74770-101">New-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="74770-101">New-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="74770-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="74770-102">SYNOPSIS</span></span>
<span data-ttu-id="74770-103">Erstellt einen Azure Web App-Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="74770-103">Creates an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74770-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="74770-104">SYNTAX</span></span>

```
New-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74770-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="74770-105">DESCRIPTION</span></span>
<span data-ttu-id="74770-106">Mit dem Cmdlet **New-AzureRmWebAppSlot** wird ein Azure Web App-Slot in einer bestimmten Ressourcengruppe erstellt, die den angegebenen app-Service Plan und das Rechenzentrum verwendet.</span><span class="sxs-lookup"><span data-stu-id="74770-106">The **New-AzureRmWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="74770-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="74770-107">EXAMPLES</span></span>

### <span data-ttu-id="74770-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="74770-108">Example 1</span></span>
```
PS C:\> New-AzureRmWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="74770-109">Dieser Befehl erstellt einen Steckplatz mit dem Namen Slot001 unter einem vorhandenen Web-App-Namen ContosoSite in der vorhandenen Ressourcengruppe Default-Web-westus in Rechenzentrum West USA.</span><span class="sxs-lookup"><span data-stu-id="74770-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="74770-110">Der Befehl verwendet einen vorhandenen APP-Service Plan mit dem Namen ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="74770-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="74770-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="74770-111">PARAMETERS</span></span>

### <span data-ttu-id="74770-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="74770-112">-AppServicePlan</span></span>
<span data-ttu-id="74770-113">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="74770-113">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74770-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="74770-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="74770-115">App-Einstellungen setzen Hashtable außer Kraft</span><span class="sxs-lookup"><span data-stu-id="74770-115">App Settings Overrides Hashtable</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74770-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="74770-116">-AseName</span></span>
<span data-ttu-id="74770-117">Name der APP-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="74770-117">App Service Environment Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74770-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74770-118">-AseResourceGroupName</span></span>
<span data-ttu-id="74770-119">Ressourcengruppen Name der APP-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="74770-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74770-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74770-120">-DefaultProfile</span></span>
<span data-ttu-id="74770-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="74770-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74770-122">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="74770-122">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="74770-123">Option "benutzerdefinierte hostnames ignorieren"</span><span class="sxs-lookup"><span data-stu-id="74770-123">Ignore Custom HostNames Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74770-124">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="74770-124">-IgnoreSourceControl</span></span>
<span data-ttu-id="74770-125">Option "Quellcodeverwaltung ignorieren"</span><span class="sxs-lookup"><span data-stu-id="74770-125">Ignore Source Control Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74770-126">-Name</span><span class="sxs-lookup"><span data-stu-id="74770-126">-Name</span></span>
<span data-ttu-id="74770-127">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="74770-127">Webapp Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74770-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74770-128">-ResourceGroupName</span></span>
<span data-ttu-id="74770-129">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="74770-129">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74770-130">-Slot</span><span class="sxs-lookup"><span data-stu-id="74770-130">-Slot</span></span>
<span data-ttu-id="74770-131">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="74770-131">Webapp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74770-132">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="74770-132">-SourceWebApp</span></span>
<span data-ttu-id="74770-133">Quell-Webobjekt</span><span class="sxs-lookup"><span data-stu-id="74770-133">Source WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74770-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74770-134">-AsJob</span></span>
<span data-ttu-id="74770-135">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="74770-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74770-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74770-136">CommonParameters</span></span>
<span data-ttu-id="74770-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74770-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74770-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74770-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74770-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="74770-139">INPUTS</span></span>

### <span data-ttu-id="74770-140">Website</span><span class="sxs-lookup"><span data-stu-id="74770-140">Site</span></span>
<span data-ttu-id="74770-141">Der Parameter "SourceWebApp" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="74770-141">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="74770-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="74770-142">OUTPUTS</span></span>

## <span data-ttu-id="74770-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="74770-143">NOTES</span></span>

## <span data-ttu-id="74770-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="74770-144">RELATED LINKS</span></span>

[<span data-ttu-id="74770-145">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="74770-145">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="74770-146">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="74770-146">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="74770-147">Neustart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="74770-147">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="74770-148">Satz-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="74770-148">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="74770-149">Anfang-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="74770-149">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="74770-150">Stopp-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="74770-150">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="74770-151">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="74770-151">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="74770-152">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="74770-152">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

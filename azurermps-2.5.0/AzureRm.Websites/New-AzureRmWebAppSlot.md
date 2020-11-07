---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: f41149c6abb946340acc06b847c72dcabcee18fe
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848967"
---
# <span data-ttu-id="7f030-101">New-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7f030-101">New-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="7f030-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7f030-102">SYNOPSIS</span></span>
<span data-ttu-id="7f030-103">Erstellt einen Azure Web App-Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="7f030-103">Creates an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f030-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f030-104">SYNTAX</span></span>

```
New-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f030-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f030-105">DESCRIPTION</span></span>
<span data-ttu-id="7f030-106">Mit dem Cmdlet **New-AzureRmWebAppSlot** wird ein Azure Web App-Slot in einer bestimmten Ressourcengruppe erstellt, die den angegebenen app-Service Plan und das Rechenzentrum verwendet.</span><span class="sxs-lookup"><span data-stu-id="7f030-106">The **New-AzureRmWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="7f030-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f030-107">EXAMPLES</span></span>

### <span data-ttu-id="7f030-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7f030-108">Example 1</span></span>
```
PS C:\> New-AzureRmWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="7f030-109">Dieser Befehl erstellt einen Steckplatz mit dem Namen Slot001 unter einem vorhandenen Web-App-Namen ContosoSite in der vorhandenen Ressourcengruppe Default-Web-westus in Rechenzentrum West USA.</span><span class="sxs-lookup"><span data-stu-id="7f030-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="7f030-110">Der Befehl verwendet einen vorhandenen APP-Service Plan mit dem Namen ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="7f030-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="7f030-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f030-111">PARAMETERS</span></span>

### <span data-ttu-id="7f030-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7f030-112">-AppServicePlan</span></span>
<span data-ttu-id="7f030-113">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="7f030-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="7f030-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="7f030-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="7f030-115">App-Einstellungen setzen Hashtable außer Kraft</span><span class="sxs-lookup"><span data-stu-id="7f030-115">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="7f030-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="7f030-116">-AseName</span></span>
<span data-ttu-id="7f030-117">Name der APP-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="7f030-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="7f030-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f030-118">-AseResourceGroupName</span></span>
<span data-ttu-id="7f030-119">Ressourcengruppen Name der APP-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="7f030-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="7f030-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f030-120">-DefaultProfile</span></span>
<span data-ttu-id="7f030-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7f030-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f030-122">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="7f030-122">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="7f030-123">Option "benutzerdefinierte hostnames ignorieren"</span><span class="sxs-lookup"><span data-stu-id="7f030-123">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="7f030-124">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="7f030-124">-IgnoreSourceControl</span></span>
<span data-ttu-id="7f030-125">Option "Quellcodeverwaltung ignorieren"</span><span class="sxs-lookup"><span data-stu-id="7f030-125">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="7f030-126">-Name</span><span class="sxs-lookup"><span data-stu-id="7f030-126">-Name</span></span>
<span data-ttu-id="7f030-127">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="7f030-127">Webapp Name</span></span>

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

### <span data-ttu-id="7f030-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f030-128">-ResourceGroupName</span></span>
<span data-ttu-id="7f030-129">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="7f030-129">Resource Group Name</span></span>

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

### <span data-ttu-id="7f030-130">-Slot</span><span class="sxs-lookup"><span data-stu-id="7f030-130">-Slot</span></span>
<span data-ttu-id="7f030-131">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="7f030-131">Webapp Slot Name</span></span>

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

### <span data-ttu-id="7f030-132">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="7f030-132">-SourceWebApp</span></span>
<span data-ttu-id="7f030-133">Quell-Webobjekt</span><span class="sxs-lookup"><span data-stu-id="7f030-133">Source WebApp Object</span></span>

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

### <span data-ttu-id="7f030-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f030-134">-AsJob</span></span>
<span data-ttu-id="7f030-135">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7f030-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7f030-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f030-136">CommonParameters</span></span>
<span data-ttu-id="7f030-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f030-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f030-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f030-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f030-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7f030-139">INPUTS</span></span>

### <span data-ttu-id="7f030-140">Website</span><span class="sxs-lookup"><span data-stu-id="7f030-140">Site</span></span>
<span data-ttu-id="7f030-141">Der Parameter "SourceWebApp" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="7f030-141">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="7f030-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7f030-142">OUTPUTS</span></span>

## <span data-ttu-id="7f030-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="7f030-143">NOTES</span></span>

## <span data-ttu-id="7f030-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7f030-144">RELATED LINKS</span></span>

[<span data-ttu-id="7f030-145">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7f030-145">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="7f030-146">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7f030-146">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="7f030-147">Neustart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7f030-147">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="7f030-148">Satz-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7f030-148">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="7f030-149">Anfang-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7f030-149">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="7f030-150">Stopp-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7f030-150">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="7f030-151">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7f030-151">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="7f030-152">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7f030-152">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

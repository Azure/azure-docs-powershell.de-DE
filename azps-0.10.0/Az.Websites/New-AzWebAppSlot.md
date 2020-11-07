---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/new-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 41851c1492c3c14e3129ba04367580b09cf3ffb5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842719"
---
# <span data-ttu-id="b6bcb-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b6bcb-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="b6bcb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b6bcb-102">SYNOPSIS</span></span>
<span data-ttu-id="b6bcb-103">Erstellt einen Azure Web App-Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="b6bcb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6bcb-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6bcb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b6bcb-105">DESCRIPTION</span></span>
<span data-ttu-id="b6bcb-106">Mit dem Cmdlet **New-AzWebAppSlot** wird ein Azure Web App-Slot in einer bestimmten Ressourcengruppe erstellt, die den angegebenen app-Service Plan und das Rechenzentrum verwendet.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="b6bcb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b6bcb-107">EXAMPLES</span></span>

### <span data-ttu-id="b6bcb-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b6bcb-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="b6bcb-109">Dieser Befehl erstellt einen Steckplatz mit dem Namen Slot001 unter einem vorhandenen Web-App-Namen ContosoSite in der vorhandenen Ressourcengruppe Default-Web-westus in Rechenzentrum West USA.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="b6bcb-110">Der Befehl verwendet einen vorhandenen APP-Service Plan mit dem Namen ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="b6bcb-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6bcb-111">PARAMETERS</span></span>

### <span data-ttu-id="b6bcb-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b6bcb-112">-AppServicePlan</span></span>
<span data-ttu-id="b6bcb-113">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="b6bcb-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="b6bcb-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="b6bcb-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="b6bcb-115">App-Einstellungen setzen Hashtable außer Kraft</span><span class="sxs-lookup"><span data-stu-id="b6bcb-115">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="b6bcb-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="b6bcb-116">-AseName</span></span>
<span data-ttu-id="b6bcb-117">Name der APP-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="b6bcb-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="b6bcb-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6bcb-118">-AseResourceGroupName</span></span>
<span data-ttu-id="b6bcb-119">Ressourcengruppen Name der APP-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="b6bcb-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="b6bcb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6bcb-120">-DefaultProfile</span></span>
<span data-ttu-id="b6bcb-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6bcb-122">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="b6bcb-122">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="b6bcb-123">Option "benutzerdefinierte hostnames ignorieren"</span><span class="sxs-lookup"><span data-stu-id="b6bcb-123">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="b6bcb-124">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="b6bcb-124">-IgnoreSourceControl</span></span>
<span data-ttu-id="b6bcb-125">Option "Quellcodeverwaltung ignorieren"</span><span class="sxs-lookup"><span data-stu-id="b6bcb-125">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="b6bcb-126">-Name</span><span class="sxs-lookup"><span data-stu-id="b6bcb-126">-Name</span></span>
<span data-ttu-id="b6bcb-127">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="b6bcb-127">Webapp Name</span></span>

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

### <span data-ttu-id="b6bcb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6bcb-128">-ResourceGroupName</span></span>
<span data-ttu-id="b6bcb-129">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="b6bcb-129">Resource Group Name</span></span>

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

### <span data-ttu-id="b6bcb-130">-Slot</span><span class="sxs-lookup"><span data-stu-id="b6bcb-130">-Slot</span></span>
<span data-ttu-id="b6bcb-131">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="b6bcb-131">Webapp Slot Name</span></span>

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

### <span data-ttu-id="b6bcb-132">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="b6bcb-132">-SourceWebApp</span></span>
<span data-ttu-id="b6bcb-133">Quell-Webobjekt</span><span class="sxs-lookup"><span data-stu-id="b6bcb-133">Source WebApp Object</span></span>

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

### <span data-ttu-id="b6bcb-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6bcb-134">-AsJob</span></span>
<span data-ttu-id="b6bcb-135">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b6bcb-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b6bcb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6bcb-136">CommonParameters</span></span>
<span data-ttu-id="b6bcb-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6bcb-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6bcb-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6bcb-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b6bcb-139">INPUTS</span></span>

### <span data-ttu-id="b6bcb-140">Website</span><span class="sxs-lookup"><span data-stu-id="b6bcb-140">Site</span></span>
<span data-ttu-id="b6bcb-141">Der Parameter "SourceWebApp" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-141">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="b6bcb-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b6bcb-142">OUTPUTS</span></span>

## <span data-ttu-id="b6bcb-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="b6bcb-143">NOTES</span></span>

## <span data-ttu-id="b6bcb-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b6bcb-144">RELATED LINKS</span></span>

[<span data-ttu-id="b6bcb-145">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b6bcb-145">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="b6bcb-146">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b6bcb-146">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="b6bcb-147">Neustart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b6bcb-147">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="b6bcb-148">Satz-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b6bcb-148">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="b6bcb-149">Anfang-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b6bcb-149">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="b6bcb-150">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b6bcb-150">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="b6bcb-151">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b6bcb-151">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="b6bcb-152">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b6bcb-152">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

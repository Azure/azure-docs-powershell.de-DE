---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotpublishingprofile
schema: 2.0.0
ms.openlocfilehash: 17ad6612ff36539d212c20c2321c6292fb63a499
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849875"
---
# <span data-ttu-id="ad2cb-101">Get-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="ad2cb-101">Get-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="ad2cb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ad2cb-102">SYNOPSIS</span></span>
<span data-ttu-id="ad2cb-103">Ruft ein Azure Web App-Slot-Veröffentlichungsprofil ab.</span><span class="sxs-lookup"><span data-stu-id="ad2cb-103">Gets an Azure Web App slot publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad2cb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad2cb-104">SYNTAX</span></span>

### <span data-ttu-id="ad2cb-105">S1</span><span class="sxs-lookup"><span data-stu-id="ad2cb-105">S1</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad2cb-106">S2</span><span class="sxs-lookup"><span data-stu-id="ad2cb-106">S2</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad2cb-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad2cb-107">DESCRIPTION</span></span>
<span data-ttu-id="ad2cb-108">Das Cmdlet " **Get-AzureRmWebAppSlotPublishingProfile** " Ruft das Web App-Veröffentlichungsprofil für den angegebenen Slot ab.</span><span class="sxs-lookup"><span data-stu-id="ad2cb-108">The **Get-AzureRmWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="ad2cb-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad2cb-109">EXAMPLES</span></span>

### <span data-ttu-id="ad2cb-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ad2cb-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="ad2cb-111">Dieser Befehl ruft das Veröffentlichungsprofil im FTP-Format für Slot Slot001 in Bezug auf das Web-App-ContosoWebApp ab, das der Ressourcengruppe Default-Web-westus zugeordnet ist, und speichert Sie in der angegebenen Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="ad2cb-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="ad2cb-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad2cb-112">PARAMETERS</span></span>

### <span data-ttu-id="ad2cb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad2cb-113">-DefaultProfile</span></span>
<span data-ttu-id="ad2cb-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ad2cb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad2cb-115">-Format</span><span class="sxs-lookup"><span data-stu-id="ad2cb-115">-Format</span></span>
<span data-ttu-id="ad2cb-116">Format</span><span class="sxs-lookup"><span data-stu-id="ad2cb-116">Format</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad2cb-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ad2cb-117">-Name</span></span>
<span data-ttu-id="ad2cb-118">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="ad2cb-118">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2cb-119">-Outputdatei</span><span class="sxs-lookup"><span data-stu-id="ad2cb-119">-OutputFile</span></span>
<span data-ttu-id="ad2cb-120">Ausgabedatei</span><span class="sxs-lookup"><span data-stu-id="ad2cb-120">Output File</span></span>

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

### <span data-ttu-id="ad2cb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad2cb-121">-ResourceGroupName</span></span>
<span data-ttu-id="ad2cb-122">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="ad2cb-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad2cb-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="ad2cb-123">-Slot</span></span>
<span data-ttu-id="ad2cb-124">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="ad2cb-124">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad2cb-125">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="ad2cb-125">-WebApp</span></span>
<span data-ttu-id="ad2cb-126">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="ad2cb-126">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2cb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad2cb-127">CommonParameters</span></span>
<span data-ttu-id="ad2cb-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad2cb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad2cb-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad2cb-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad2cb-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ad2cb-130">INPUTS</span></span>

### <span data-ttu-id="ad2cb-131">Website</span><span class="sxs-lookup"><span data-stu-id="ad2cb-131">Site</span></span>
<span data-ttu-id="ad2cb-132">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ad2cb-132">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ad2cb-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ad2cb-133">OUTPUTS</span></span>

## <span data-ttu-id="ad2cb-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="ad2cb-134">NOTES</span></span>

## <span data-ttu-id="ad2cb-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ad2cb-135">RELATED LINKS</span></span>

[<span data-ttu-id="ad2cb-136">Reset-AzureRMWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="ad2cb-136">Reset-AzureRMWebAppSlotPublishingProfile</span></span>](./Reset-AzureRmWebAppSlotPublishingProfile.md)

[<span data-ttu-id="ad2cb-137">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ad2cb-137">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="ad2cb-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ad2cb-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

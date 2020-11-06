---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: 1202d15504717052513f1ef77a21e008fefe20af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478133"
---
# <span data-ttu-id="0b98d-101">Get-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="0b98d-101">Get-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="0b98d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0b98d-102">SYNOPSIS</span></span>
<span data-ttu-id="0b98d-103">Ruft ein Azure Web App-Veröffentlichungsprofil ab.</span><span class="sxs-lookup"><span data-stu-id="0b98d-103">Gets an Azure Web App publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b98d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b98d-104">SYNTAX</span></span>

### <span data-ttu-id="0b98d-105">S1</span><span class="sxs-lookup"><span data-stu-id="0b98d-105">S1</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b98d-106">S2</span><span class="sxs-lookup"><span data-stu-id="0b98d-106">S2</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b98d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b98d-107">DESCRIPTION</span></span>
<span data-ttu-id="0b98d-108">Das Cmdlet " **Get-AzureRmWebAppPublishingProfile** " Ruft ein Azure Web App-Veröffentlichungsprofil ab.</span><span class="sxs-lookup"><span data-stu-id="0b98d-108">The **Get-AzureRmWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="0b98d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b98d-109">EXAMPLES</span></span>

### <span data-ttu-id="0b98d-110">1:</span><span class="sxs-lookup"><span data-stu-id="0b98d-110">1:</span></span>
```
PS C:\> Get-AzureRmWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="0b98d-111">Dieser Befehl ruft das Veröffentlichungsprofil im FTP-Format für Web App-ContosoWebApp ab, das der Ressourcengruppe Default-Web-westus zugeordnet ist, und speichert Sie in der angegebenen Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="0b98d-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="0b98d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b98d-112">PARAMETERS</span></span>

### <span data-ttu-id="0b98d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b98d-113">-DefaultProfile</span></span>
<span data-ttu-id="0b98d-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0b98d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b98d-115">-Format</span><span class="sxs-lookup"><span data-stu-id="0b98d-115">-Format</span></span>
<span data-ttu-id="0b98d-116">Format</span><span class="sxs-lookup"><span data-stu-id="0b98d-116">Format</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b98d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0b98d-117">-Name</span></span>
<span data-ttu-id="0b98d-118">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="0b98d-118">WebApp Name</span></span>

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

### <span data-ttu-id="0b98d-119">-Outputdatei</span><span class="sxs-lookup"><span data-stu-id="0b98d-119">-OutputFile</span></span>
<span data-ttu-id="0b98d-120">Ausgabedatei</span><span class="sxs-lookup"><span data-stu-id="0b98d-120">Output File</span></span>

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

### <span data-ttu-id="0b98d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b98d-121">-ResourceGroupName</span></span>
<span data-ttu-id="0b98d-122">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="0b98d-122">Resource Group Name</span></span>

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

### <span data-ttu-id="0b98d-123">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="0b98d-123">-WebApp</span></span>
<span data-ttu-id="0b98d-124">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="0b98d-124">WebApp Object</span></span>

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

### <span data-ttu-id="0b98d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b98d-125">CommonParameters</span></span>
<span data-ttu-id="0b98d-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b98d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b98d-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b98d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b98d-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0b98d-128">INPUTS</span></span>

### <span data-ttu-id="0b98d-129">Website</span><span class="sxs-lookup"><span data-stu-id="0b98d-129">Site</span></span>
<span data-ttu-id="0b98d-130">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0b98d-130">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="0b98d-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0b98d-131">OUTPUTS</span></span>

## <span data-ttu-id="0b98d-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="0b98d-132">NOTES</span></span>

## <span data-ttu-id="0b98d-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0b98d-133">RELATED LINKS</span></span>

[<span data-ttu-id="0b98d-134">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0b98d-134">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="0b98d-135">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0b98d-135">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)



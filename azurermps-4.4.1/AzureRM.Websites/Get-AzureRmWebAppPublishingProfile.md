---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: a05dfcbf509ccb68c0b928467a5695361a4916e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481393"
---
# <span data-ttu-id="f53a0-101">Get-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="f53a0-101">Get-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="f53a0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f53a0-102">SYNOPSIS</span></span>
<span data-ttu-id="f53a0-103">Ruft ein Azure Web App-Veröffentlichungsprofil ab.</span><span class="sxs-lookup"><span data-stu-id="f53a0-103">Gets an Azure Web App publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f53a0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f53a0-104">SYNTAX</span></span>

### <span data-ttu-id="f53a0-105">S1</span><span class="sxs-lookup"><span data-stu-id="f53a0-105">S1</span></span>
```
Get-AzureRmWebAppPublishingProfile [-OutputFile] <String> [[-Format] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f53a0-106">S2</span><span class="sxs-lookup"><span data-stu-id="f53a0-106">S2</span></span>
```
Get-AzureRmWebAppPublishingProfile [-OutputFile] <String> [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f53a0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f53a0-107">DESCRIPTION</span></span>
<span data-ttu-id="f53a0-108">Das Cmdlet " **Get-AzureRmWebAppPublishingProfile** " Ruft ein Azure Web App-Veröffentlichungsprofil ab.</span><span class="sxs-lookup"><span data-stu-id="f53a0-108">The **Get-AzureRmWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="f53a0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f53a0-109">EXAMPLES</span></span>

### <span data-ttu-id="f53a0-110">1:</span><span class="sxs-lookup"><span data-stu-id="f53a0-110">1:</span></span>
```
PS C:\> Get-AzureRmWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="f53a0-111">Dieser Befehl ruft das Veröffentlichungsprofil im FTP-Format für Web App-ContosoWebApp ab, das der Ressourcengruppe Default-Web-westus zugeordnet ist, und speichert Sie in der angegebenen Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="f53a0-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="f53a0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f53a0-112">PARAMETERS</span></span>

### <span data-ttu-id="f53a0-113">-Format</span><span class="sxs-lookup"><span data-stu-id="f53a0-113">-Format</span></span>
<span data-ttu-id="f53a0-114">Format</span><span class="sxs-lookup"><span data-stu-id="f53a0-114">Format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f53a0-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f53a0-115">-Name</span></span>
<span data-ttu-id="f53a0-116">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="f53a0-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f53a0-117">-Outputdatei</span><span class="sxs-lookup"><span data-stu-id="f53a0-117">-OutputFile</span></span>
<span data-ttu-id="f53a0-118">Ausgabedatei</span><span class="sxs-lookup"><span data-stu-id="f53a0-118">Output File</span></span>

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

### <span data-ttu-id="f53a0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f53a0-119">-ResourceGroupName</span></span>
<span data-ttu-id="f53a0-120">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="f53a0-120">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f53a0-121">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="f53a0-121">-WebApp</span></span>
<span data-ttu-id="f53a0-122">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="f53a0-122">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f53a0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f53a0-123">-DefaultProfile</span></span>
<span data-ttu-id="f53a0-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f53a0-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f53a0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f53a0-125">CommonParameters</span></span>
<span data-ttu-id="f53a0-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f53a0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f53a0-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f53a0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f53a0-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f53a0-128">INPUTS</span></span>

### <span data-ttu-id="f53a0-129">Website</span><span class="sxs-lookup"><span data-stu-id="f53a0-129">Site</span></span>
<span data-ttu-id="f53a0-130">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="f53a0-130">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f53a0-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f53a0-131">OUTPUTS</span></span>

## <span data-ttu-id="f53a0-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="f53a0-132">NOTES</span></span>

## <span data-ttu-id="f53a0-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f53a0-133">RELATED LINKS</span></span>

[<span data-ttu-id="f53a0-134">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f53a0-134">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="f53a0-135">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f53a0-135">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)



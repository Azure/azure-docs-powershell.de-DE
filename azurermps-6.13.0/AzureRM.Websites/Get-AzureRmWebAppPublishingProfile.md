---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: a59d747dd7ba91d69d364770c91baf1a21ffedd9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481913"
---
# <span data-ttu-id="fea4a-101">Get-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="fea4a-101">Get-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="fea4a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fea4a-102">SYNOPSIS</span></span>
<span data-ttu-id="fea4a-103">Ruft ein Azure Web App-Veröffentlichungsprofil ab.</span><span class="sxs-lookup"><span data-stu-id="fea4a-103">Gets an Azure Web App publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fea4a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fea4a-104">SYNTAX</span></span>

### <span data-ttu-id="fea4a-105">S1</span><span class="sxs-lookup"><span data-stu-id="fea4a-105">S1</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fea4a-106">S2</span><span class="sxs-lookup"><span data-stu-id="fea4a-106">S2</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fea4a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fea4a-107">DESCRIPTION</span></span>
<span data-ttu-id="fea4a-108">Das Cmdlet " **Get-AzureRmWebAppPublishingProfile** " Ruft ein Azure Web App-Veröffentlichungsprofil ab.</span><span class="sxs-lookup"><span data-stu-id="fea4a-108">The **Get-AzureRmWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="fea4a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fea4a-109">EXAMPLES</span></span>

### <span data-ttu-id="fea4a-110">1:</span><span class="sxs-lookup"><span data-stu-id="fea4a-110">1:</span></span>
```
PS C:\> Get-AzureRmWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="fea4a-111">Dieser Befehl ruft das Veröffentlichungsprofil im FTP-Format für Web App-ContosoWebApp ab, das der Ressourcengruppe Default-Web-westus zugeordnet ist, und speichert Sie in der angegebenen Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="fea4a-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="fea4a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fea4a-112">PARAMETERS</span></span>

### <span data-ttu-id="fea4a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fea4a-113">-DefaultProfile</span></span>
<span data-ttu-id="fea4a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fea4a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fea4a-115">-Format</span><span class="sxs-lookup"><span data-stu-id="fea4a-115">-Format</span></span>
<span data-ttu-id="fea4a-116">Format</span><span class="sxs-lookup"><span data-stu-id="fea4a-116">Format</span></span>

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

### <span data-ttu-id="fea4a-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="fea4a-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="fea4a-118">Einbeziehen der Disaster Recovery-Endpunkte bei true</span><span class="sxs-lookup"><span data-stu-id="fea4a-118">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: None
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fea4a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="fea4a-119">-Name</span></span>
<span data-ttu-id="fea4a-120">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="fea4a-120">WebApp Name</span></span>

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

### <span data-ttu-id="fea4a-121">-Outputdatei</span><span class="sxs-lookup"><span data-stu-id="fea4a-121">-OutputFile</span></span>
<span data-ttu-id="fea4a-122">Ausgabedatei</span><span class="sxs-lookup"><span data-stu-id="fea4a-122">Output File</span></span>

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

### <span data-ttu-id="fea4a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fea4a-123">-ResourceGroupName</span></span>
<span data-ttu-id="fea4a-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="fea4a-124">Resource Group Name</span></span>

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

### <span data-ttu-id="fea4a-125">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="fea4a-125">-WebApp</span></span>
<span data-ttu-id="fea4a-126">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="fea4a-126">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fea4a-127">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="fea4a-127">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="fea4a-128">Einbeziehen der Disaster Recovery-Endpunkte bei true</span><span class="sxs-lookup"><span data-stu-id="fea4a-128">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: None
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fea4a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fea4a-129">CommonParameters</span></span>
<span data-ttu-id="fea4a-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fea4a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fea4a-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fea4a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fea4a-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fea4a-132">INPUTS</span></span>

### <span data-ttu-id="fea4a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fea4a-133">System.String</span></span>

### <span data-ttu-id="fea4a-134">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="fea4a-134">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="fea4a-135">Parameter: webByValue</span><span class="sxs-lookup"><span data-stu-id="fea4a-135">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="fea4a-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fea4a-136">OUTPUTS</span></span>

### <span data-ttu-id="fea4a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="fea4a-137">System.String</span></span>

## <span data-ttu-id="fea4a-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="fea4a-138">NOTES</span></span>

## <span data-ttu-id="fea4a-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fea4a-139">RELATED LINKS</span></span>

[<span data-ttu-id="fea4a-140">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="fea4a-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="fea4a-141">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fea4a-141">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)



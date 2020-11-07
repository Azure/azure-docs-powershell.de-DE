---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: 426fc5c6cac67da7b0380b3a5e5e40cc1b533366
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663278"
---
# <span data-ttu-id="9e1bc-101">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e1bc-101">Get-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="9e1bc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9e1bc-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e1bc-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e1bc-103">SYNTAX</span></span>

### <span data-ttu-id="9e1bc-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="9e1bc-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e1bc-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="9e1bc-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e1bc-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e1bc-106">DESCRIPTION</span></span>
<span data-ttu-id="9e1bc-107">Das Cmdlet " **Get-AzureRmWebAppBackupConfiguration** " Ruft die Sicherungskonfiguration einer Azure Web App ab.</span><span class="sxs-lookup"><span data-stu-id="9e1bc-107">The **Get-AzureRmWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="9e1bc-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9e1bc-108">EXAMPLES</span></span>

### <span data-ttu-id="9e1bc-109">1:</span><span class="sxs-lookup"><span data-stu-id="9e1bc-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="9e1bc-110">Dieser Befehl ruft die Sicherungskonfiguration aus der Web-App mit dem Namen WebAppStandard ab, die zur Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="9e1bc-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="9e1bc-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e1bc-111">PARAMETERS</span></span>

### <span data-ttu-id="9e1bc-112">-Name</span><span class="sxs-lookup"><span data-stu-id="9e1bc-112">-Name</span></span>
<span data-ttu-id="9e1bc-113">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="9e1bc-113">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e1bc-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e1bc-114">-ResourceGroupName</span></span>
<span data-ttu-id="9e1bc-115">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="9e1bc-115">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e1bc-116">-Slot</span><span class="sxs-lookup"><span data-stu-id="9e1bc-116">-Slot</span></span>
<span data-ttu-id="9e1bc-117">Name des Steckplatzes</span><span class="sxs-lookup"><span data-stu-id="9e1bc-117">Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e1bc-118">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="9e1bc-118">-WebApp</span></span>
<span data-ttu-id="9e1bc-119">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="9e1bc-119">WebApp Name</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e1bc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e1bc-120">-DefaultProfile</span></span>
<span data-ttu-id="9e1bc-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9e1bc-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e1bc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e1bc-122">CommonParameters</span></span>
<span data-ttu-id="9e1bc-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e1bc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e1bc-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e1bc-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e1bc-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9e1bc-125">INPUTS</span></span>

### <span data-ttu-id="9e1bc-126">Website</span><span class="sxs-lookup"><span data-stu-id="9e1bc-126">Site</span></span>
<span data-ttu-id="9e1bc-127">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="9e1bc-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="9e1bc-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9e1bc-128">OUTPUTS</span></span>

### <span data-ttu-id="9e1bc-129">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e1bc-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="9e1bc-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="9e1bc-130">NOTES</span></span>

## <span data-ttu-id="9e1bc-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9e1bc-131">RELATED LINKS</span></span>


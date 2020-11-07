---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: 81c9d87ecd93097c7e114a312b68d25d7dd681c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662292"
---
# <span data-ttu-id="7b79f-101">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b79f-101">Get-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="7b79f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7b79f-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b79f-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b79f-103">SYNTAX</span></span>

### <span data-ttu-id="7b79f-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="7b79f-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b79f-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="7b79f-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7b79f-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b79f-106">DESCRIPTION</span></span>
<span data-ttu-id="7b79f-107">Das Cmdlet " **Get-AzureRmWebAppBackupConfiguration** " Ruft die Sicherungskonfiguration einer Azure Web App ab.</span><span class="sxs-lookup"><span data-stu-id="7b79f-107">The **Get-AzureRmWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="7b79f-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7b79f-108">EXAMPLES</span></span>

### <span data-ttu-id="7b79f-109">1:</span><span class="sxs-lookup"><span data-stu-id="7b79f-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="7b79f-110">Dieser Befehl ruft die Sicherungskonfiguration aus der Web-App mit dem Namen WebAppStandard ab, die zur Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="7b79f-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="7b79f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b79f-111">PARAMETERS</span></span>

### <span data-ttu-id="7b79f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b79f-112">-DefaultProfile</span></span>
<span data-ttu-id="7b79f-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7b79f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b79f-114">-Name</span><span class="sxs-lookup"><span data-stu-id="7b79f-114">-Name</span></span>
<span data-ttu-id="7b79f-115">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="7b79f-115">WebApp Name</span></span>

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

### <span data-ttu-id="7b79f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b79f-116">-ResourceGroupName</span></span>
<span data-ttu-id="7b79f-117">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="7b79f-117">Resource Group Name</span></span>

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

### <span data-ttu-id="7b79f-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="7b79f-118">-Slot</span></span>
<span data-ttu-id="7b79f-119">Name des Steckplatzes</span><span class="sxs-lookup"><span data-stu-id="7b79f-119">Slot Name</span></span>

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

### <span data-ttu-id="7b79f-120">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="7b79f-120">-WebApp</span></span>
<span data-ttu-id="7b79f-121">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="7b79f-121">WebApp Name</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b79f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b79f-122">CommonParameters</span></span>
<span data-ttu-id="7b79f-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b79f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b79f-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b79f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b79f-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7b79f-125">INPUTS</span></span>

### <span data-ttu-id="7b79f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7b79f-126">System.String</span></span>

### <span data-ttu-id="7b79f-127">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="7b79f-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="7b79f-128">Parameter: webByValue</span><span class="sxs-lookup"><span data-stu-id="7b79f-128">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="7b79f-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7b79f-129">OUTPUTS</span></span>

### <span data-ttu-id="7b79f-130">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b79f-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="7b79f-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="7b79f-131">NOTES</span></span>

## <span data-ttu-id="7b79f-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7b79f-132">RELATED LINKS</span></span>

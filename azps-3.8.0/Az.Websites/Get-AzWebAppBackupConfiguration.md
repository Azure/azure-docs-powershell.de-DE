---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
ms.openlocfilehash: e371beefd521e5a10a4450209393a2f8bdb7b790
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845760"
---
# <span data-ttu-id="777a3-101">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="777a3-101">Get-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="777a3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="777a3-102">SYNOPSIS</span></span>

## <span data-ttu-id="777a3-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="777a3-103">SYNTAX</span></span>

### <span data-ttu-id="777a3-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="777a3-104">FromResourceName</span></span>
```
Get-AzWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="777a3-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="777a3-105">FromWebApp</span></span>
```
Get-AzWebAppBackupConfiguration [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="777a3-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="777a3-106">DESCRIPTION</span></span>
<span data-ttu-id="777a3-107">Das Cmdlet " **Get-AzWebAppBackupConfiguration** " Ruft die Sicherungskonfiguration einer Azure Web App ab.</span><span class="sxs-lookup"><span data-stu-id="777a3-107">The **Get-AzWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="777a3-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="777a3-108">EXAMPLES</span></span>

### <span data-ttu-id="777a3-109">1:</span><span class="sxs-lookup"><span data-stu-id="777a3-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="777a3-110">Dieser Befehl ruft die Sicherungskonfiguration aus der Web-App mit dem Namen WebAppStandard ab, die zur Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="777a3-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="777a3-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="777a3-111">PARAMETERS</span></span>

### <span data-ttu-id="777a3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="777a3-112">-DefaultProfile</span></span>
<span data-ttu-id="777a3-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="777a3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="777a3-114">-Name</span><span class="sxs-lookup"><span data-stu-id="777a3-114">-Name</span></span>
<span data-ttu-id="777a3-115">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="777a3-115">WebApp Name</span></span>

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

### <span data-ttu-id="777a3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="777a3-116">-ResourceGroupName</span></span>
<span data-ttu-id="777a3-117">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="777a3-117">Resource Group Name</span></span>

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

### <span data-ttu-id="777a3-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="777a3-118">-Slot</span></span>
<span data-ttu-id="777a3-119">Name des Steckplatzes</span><span class="sxs-lookup"><span data-stu-id="777a3-119">Slot Name</span></span>

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

### <span data-ttu-id="777a3-120">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="777a3-120">-WebApp</span></span>
<span data-ttu-id="777a3-121">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="777a3-121">WebApp Name</span></span>

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

### <span data-ttu-id="777a3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="777a3-122">CommonParameters</span></span>
<span data-ttu-id="777a3-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="777a3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="777a3-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="777a3-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="777a3-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="777a3-125">INPUTS</span></span>

### <span data-ttu-id="777a3-126">System. String</span><span class="sxs-lookup"><span data-stu-id="777a3-126">System.String</span></span>

### <span data-ttu-id="777a3-127">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="777a3-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="777a3-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="777a3-128">OUTPUTS</span></span>

### <span data-ttu-id="777a3-129">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="777a3-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="777a3-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="777a3-130">NOTES</span></span>

## <span data-ttu-id="777a3-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="777a3-131">RELATED LINKS</span></span>

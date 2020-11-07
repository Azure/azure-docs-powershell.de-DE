---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 4c6dc810d35feedd0d0d43e0bd3b3efb7c9b6641
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842792"
---
# <span data-ttu-id="62fd1-101">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="62fd1-101">Get-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="62fd1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="62fd1-102">SYNOPSIS</span></span>

## <span data-ttu-id="62fd1-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="62fd1-103">SYNTAX</span></span>

### <span data-ttu-id="62fd1-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="62fd1-104">FromResourceName</span></span>
```
Get-AzWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62fd1-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="62fd1-105">FromWebApp</span></span>
```
Get-AzWebAppBackupConfiguration [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="62fd1-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="62fd1-106">DESCRIPTION</span></span>
<span data-ttu-id="62fd1-107">Das Cmdlet " **Get-AzWebAppBackupConfiguration** " Ruft die Sicherungskonfiguration einer Azure Web App ab.</span><span class="sxs-lookup"><span data-stu-id="62fd1-107">The **Get-AzWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="62fd1-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="62fd1-108">EXAMPLES</span></span>

### <span data-ttu-id="62fd1-109">1:</span><span class="sxs-lookup"><span data-stu-id="62fd1-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="62fd1-110">Dieser Befehl ruft die Sicherungskonfiguration aus der Web-App mit dem Namen WebAppStandard ab, die zur Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="62fd1-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="62fd1-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="62fd1-111">PARAMETERS</span></span>

### <span data-ttu-id="62fd1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62fd1-112">-DefaultProfile</span></span>
<span data-ttu-id="62fd1-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="62fd1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62fd1-114">-Name</span><span class="sxs-lookup"><span data-stu-id="62fd1-114">-Name</span></span>
<span data-ttu-id="62fd1-115">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="62fd1-115">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fd1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62fd1-116">-ResourceGroupName</span></span>
<span data-ttu-id="62fd1-117">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="62fd1-117">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fd1-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="62fd1-118">-Slot</span></span>
<span data-ttu-id="62fd1-119">Name des Steckplatzes</span><span class="sxs-lookup"><span data-stu-id="62fd1-119">Slot Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fd1-120">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="62fd1-120">-WebApp</span></span>
<span data-ttu-id="62fd1-121">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="62fd1-121">WebApp Name</span></span>

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62fd1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62fd1-122">CommonParameters</span></span>
<span data-ttu-id="62fd1-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62fd1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62fd1-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62fd1-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62fd1-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="62fd1-125">INPUTS</span></span>

### <span data-ttu-id="62fd1-126">Website</span><span class="sxs-lookup"><span data-stu-id="62fd1-126">Site</span></span>
<span data-ttu-id="62fd1-127">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="62fd1-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="62fd1-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="62fd1-128">OUTPUTS</span></span>

### <span data-ttu-id="62fd1-129">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="62fd1-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="62fd1-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="62fd1-130">NOTES</span></span>

## <span data-ttu-id="62fd1-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="62fd1-131">RELATED LINKS</span></span>


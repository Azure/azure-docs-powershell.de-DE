---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackup.md
ms.openlocfilehash: b533d63e83d731dd5b95788609d32fa4cf7863f5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842795"
---
# <span data-ttu-id="60c96-101">Get-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="60c96-101">Get-AzWebAppBackup</span></span>

## <span data-ttu-id="60c96-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="60c96-102">SYNOPSIS</span></span>

## <span data-ttu-id="60c96-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="60c96-103">SYNTAX</span></span>

### <span data-ttu-id="60c96-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="60c96-104">FromResourceName</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60c96-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="60c96-105">FromWebApp</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="60c96-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60c96-106">DESCRIPTION</span></span>
<span data-ttu-id="60c96-107">Das Cmdlet " **Get-AzWebAppBackup** " Ruft die angegebene Sicherung einer Azure Web App ab.</span><span class="sxs-lookup"><span data-stu-id="60c96-107">The **Get-AzWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="60c96-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="60c96-108">EXAMPLES</span></span>

### <span data-ttu-id="60c96-109">1:</span><span class="sxs-lookup"><span data-stu-id="60c96-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="60c96-110">Dieser Befehl ruft die Sicherung mit der ID "12345" aus der Web-App mit dem Namen WebAppStandard ab, die zur Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="60c96-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="60c96-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="60c96-111">PARAMETERS</span></span>

### <span data-ttu-id="60c96-112">-Backup-Nr.</span><span class="sxs-lookup"><span data-stu-id="60c96-112">-BackupId</span></span>
<span data-ttu-id="60c96-113">Sicherungs-ID</span><span class="sxs-lookup"><span data-stu-id="60c96-113">Backup Id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60c96-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60c96-114">-DefaultProfile</span></span>
<span data-ttu-id="60c96-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="60c96-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60c96-116">-Name</span><span class="sxs-lookup"><span data-stu-id="60c96-116">-Name</span></span>
<span data-ttu-id="60c96-117">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="60c96-117">Webapp Name</span></span>

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

### <span data-ttu-id="60c96-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60c96-118">-ResourceGroupName</span></span>
<span data-ttu-id="60c96-119">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="60c96-119">Resource Group Name</span></span>

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

### <span data-ttu-id="60c96-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="60c96-120">-Slot</span></span>
<span data-ttu-id="60c96-121">Name des Steckplatzes</span><span class="sxs-lookup"><span data-stu-id="60c96-121">Slot Name</span></span>

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

### <span data-ttu-id="60c96-122">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="60c96-122">-WebApp</span></span>
<span data-ttu-id="60c96-123">Pipelining</span><span class="sxs-lookup"><span data-stu-id="60c96-123">Piped WebApp</span></span>

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

### <span data-ttu-id="60c96-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60c96-124">CommonParameters</span></span>
<span data-ttu-id="60c96-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60c96-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60c96-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60c96-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60c96-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="60c96-127">INPUTS</span></span>

### <span data-ttu-id="60c96-128">Website</span><span class="sxs-lookup"><span data-stu-id="60c96-128">Site</span></span>
<span data-ttu-id="60c96-129">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="60c96-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="60c96-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="60c96-130">OUTPUTS</span></span>

### <span data-ttu-id="60c96-131">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="60c96-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="60c96-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="60c96-132">NOTES</span></span>

## <span data-ttu-id="60c96-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="60c96-133">RELATED LINKS</span></span>


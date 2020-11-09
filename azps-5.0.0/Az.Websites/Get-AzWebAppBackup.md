---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
ms.openlocfilehash: e8c3f7543062613527e7f52be2cd6493f53c5f60
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300898"
---
# <span data-ttu-id="a9b3a-101">Get-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="a9b3a-101">Get-AzWebAppBackup</span></span>

## <span data-ttu-id="a9b3a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9b3a-102">SYNOPSIS</span></span>

## <span data-ttu-id="a9b3a-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9b3a-103">SYNTAX</span></span>

### <span data-ttu-id="a9b3a-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="a9b3a-104">FromResourceName</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9b3a-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="a9b3a-105">FromWebApp</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9b3a-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9b3a-106">DESCRIPTION</span></span>
<span data-ttu-id="a9b3a-107">Das Cmdlet " **Get-AzWebAppBackup** " Ruft die angegebene Sicherung einer Azure Web App ab.</span><span class="sxs-lookup"><span data-stu-id="a9b3a-107">The **Get-AzWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="a9b3a-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9b3a-108">EXAMPLES</span></span>

### <span data-ttu-id="a9b3a-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a9b3a-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="a9b3a-110">Dieser Befehl ruft die Sicherung mit der ID "12345" aus der Web-App mit dem Namen WebAppStandard ab, die zur Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="a9b3a-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="a9b3a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9b3a-111">PARAMETERS</span></span>

### <span data-ttu-id="a9b3a-112">-Backup-Nr.</span><span class="sxs-lookup"><span data-stu-id="a9b3a-112">-BackupId</span></span>
<span data-ttu-id="a9b3a-113">Sicherungs-ID</span><span class="sxs-lookup"><span data-stu-id="a9b3a-113">Backup Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9b3a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9b3a-114">-DefaultProfile</span></span>
<span data-ttu-id="a9b3a-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a9b3a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9b3a-116">-Name</span><span class="sxs-lookup"><span data-stu-id="a9b3a-116">-Name</span></span>
<span data-ttu-id="a9b3a-117">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="a9b3a-117">Webapp Name</span></span>

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

### <span data-ttu-id="a9b3a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9b3a-118">-ResourceGroupName</span></span>
<span data-ttu-id="a9b3a-119">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="a9b3a-119">Resource Group Name</span></span>

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

### <span data-ttu-id="a9b3a-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="a9b3a-120">-Slot</span></span>
<span data-ttu-id="a9b3a-121">Name des Steckplatzes</span><span class="sxs-lookup"><span data-stu-id="a9b3a-121">Slot Name</span></span>

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

### <span data-ttu-id="a9b3a-122">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="a9b3a-122">-WebApp</span></span>
<span data-ttu-id="a9b3a-123">Pipelining</span><span class="sxs-lookup"><span data-stu-id="a9b3a-123">Piped WebApp</span></span>

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

### <span data-ttu-id="a9b3a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9b3a-124">CommonParameters</span></span>
<span data-ttu-id="a9b3a-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9b3a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9b3a-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9b3a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9b3a-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9b3a-127">INPUTS</span></span>

### <span data-ttu-id="a9b3a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a9b3a-128">System.String</span></span>

### <span data-ttu-id="a9b3a-129">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="a9b3a-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a9b3a-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9b3a-130">OUTPUTS</span></span>

### <span data-ttu-id="a9b3a-131">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="a9b3a-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="a9b3a-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9b3a-132">NOTES</span></span>

## <span data-ttu-id="a9b3a-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9b3a-133">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: 1374bfb67b3150b2c65841d91fd440a83f791b95
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842768"
---
# <span data-ttu-id="24eef-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="24eef-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="24eef-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="24eef-102">SYNOPSIS</span></span>
<span data-ttu-id="24eef-103">Ruft die für eine Web-App verfügbaren Snapshots ab.</span><span class="sxs-lookup"><span data-stu-id="24eef-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="24eef-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="24eef-104">SYNTAX</span></span>

### <span data-ttu-id="24eef-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="24eef-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="24eef-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="24eef-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="24eef-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="24eef-107">DESCRIPTION</span></span>
<span data-ttu-id="24eef-108">Das Cmdlet " **Get-AzWebAppSnapshot** " gibt alle Snapshots für eine Web-App zurück.</span><span class="sxs-lookup"><span data-stu-id="24eef-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="24eef-109">Schnappschüsse sind automatische Sicherungen der Dateien und Einstellungen einer Web-App.</span><span class="sxs-lookup"><span data-stu-id="24eef-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="24eef-110">Eine Momentaufnahme kann mit dem Cmdlet **Restore-AzWebAppSnapshot** wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="24eef-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="24eef-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="24eef-111">EXAMPLES</span></span>

### <span data-ttu-id="24eef-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="24eef-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="24eef-113">Abrufen der Snapshots für eine Web-App mit dem Namen "ConstosoApp" mit einem Slot mit dem Namen "Staging" in der Ressourcengruppe "Standard-Web-westus"</span><span class="sxs-lookup"><span data-stu-id="24eef-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="24eef-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="24eef-114">PARAMETERS</span></span>

### <span data-ttu-id="24eef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24eef-115">-DefaultProfile</span></span>
<span data-ttu-id="24eef-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="24eef-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24eef-117">-Name</span><span class="sxs-lookup"><span data-stu-id="24eef-117">-Name</span></span>
<span data-ttu-id="24eef-118">Der Name der Web-App.</span><span class="sxs-lookup"><span data-stu-id="24eef-118">The name of the web app.</span></span>

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

### <span data-ttu-id="24eef-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24eef-119">-ResourceGroupName</span></span>
<span data-ttu-id="24eef-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="24eef-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="24eef-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="24eef-121">-Slot</span></span>
<span data-ttu-id="24eef-122">Der Name des Web App-Slots.</span><span class="sxs-lookup"><span data-stu-id="24eef-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="24eef-123">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="24eef-123">-WebApp</span></span>
<span data-ttu-id="24eef-124">Das Web App-Objekt</span><span class="sxs-lookup"><span data-stu-id="24eef-124">The web app object</span></span>

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

## <span data-ttu-id="24eef-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="24eef-125">INPUTS</span></span>

### <span data-ttu-id="24eef-126">System. String</span><span class="sxs-lookup"><span data-stu-id="24eef-126">System.String</span></span>
<span data-ttu-id="24eef-127">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="24eef-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>


## <span data-ttu-id="24eef-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="24eef-128">OUTPUTS</span></span>

### <span data-ttu-id="24eef-129">Microsoft. Azure. Commands. webapps. Cmdlets. backuprestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="24eef-129">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>


## <span data-ttu-id="24eef-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="24eef-130">NOTES</span></span>

## <span data-ttu-id="24eef-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="24eef-131">RELATED LINKS</span></span>


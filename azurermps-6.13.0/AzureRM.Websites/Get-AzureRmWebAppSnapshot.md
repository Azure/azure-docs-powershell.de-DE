---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSnapshot.md
ms.openlocfilehash: 292364ae6355c640ed66116c84289fe303acdd53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93475858"
---
# <span data-ttu-id="a4a1c-101">Get-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="a4a1c-101">Get-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="a4a1c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a4a1c-102">SYNOPSIS</span></span>
<span data-ttu-id="a4a1c-103">Ruft die für eine Web-App verfügbaren Snapshots ab.</span><span class="sxs-lookup"><span data-stu-id="a4a1c-103">Gets the snapshots available for a web app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4a1c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4a1c-104">SYNTAX</span></span>

### <span data-ttu-id="a4a1c-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="a4a1c-105">FromResourceName</span></span>
```
Get-AzureRmWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4a1c-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="a4a1c-106">FromWebApp</span></span>
```
Get-AzureRmWebAppSnapshot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4a1c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a4a1c-107">DESCRIPTION</span></span>
<span data-ttu-id="a4a1c-108">Das Cmdlet " **Get-AzureRmWebAppSnapshot** " gibt alle Snapshots für eine Web-App zurück.</span><span class="sxs-lookup"><span data-stu-id="a4a1c-108">The **Get-AzureRmWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="a4a1c-109">Schnappschüsse sind automatische Sicherungen der Dateien und Einstellungen einer Web-App.</span><span class="sxs-lookup"><span data-stu-id="a4a1c-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="a4a1c-110">Eine Momentaufnahme kann mit dem Cmdlet **Restore-AzureRmWebAppSnapshot** wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a4a1c-110">A snapshot can be restored with the **Restore-AzureRmWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="a4a1c-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a4a1c-111">EXAMPLES</span></span>

### <span data-ttu-id="a4a1c-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a4a1c-112">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="a4a1c-113">Abrufen der Snapshots für eine Web-App mit dem Namen "ConstosoApp" mit einem Slot mit dem Namen "Staging" in der Ressourcengruppe "Standard-Web-westus"</span><span class="sxs-lookup"><span data-stu-id="a4a1c-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="a4a1c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4a1c-114">PARAMETERS</span></span>

### <span data-ttu-id="a4a1c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4a1c-115">-DefaultProfile</span></span>
<span data-ttu-id="a4a1c-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a4a1c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4a1c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a4a1c-117">-Name</span></span>
<span data-ttu-id="a4a1c-118">Der Name der Web-App.</span><span class="sxs-lookup"><span data-stu-id="a4a1c-118">The name of the web app.</span></span>

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

### <span data-ttu-id="a4a1c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4a1c-119">-ResourceGroupName</span></span>
<span data-ttu-id="a4a1c-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a4a1c-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="a4a1c-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="a4a1c-121">-Slot</span></span>
<span data-ttu-id="a4a1c-122">Der Name des Web App-Slots.</span><span class="sxs-lookup"><span data-stu-id="a4a1c-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="a4a1c-123">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="a4a1c-123">-WebApp</span></span>
<span data-ttu-id="a4a1c-124">Das Web App-Objekt</span><span class="sxs-lookup"><span data-stu-id="a4a1c-124">The web app object</span></span>

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

### <span data-ttu-id="a4a1c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4a1c-125">CommonParameters</span></span>
<span data-ttu-id="a4a1c-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4a1c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4a1c-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4a1c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4a1c-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a4a1c-128">INPUTS</span></span>

### <span data-ttu-id="a4a1c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a4a1c-129">System.String</span></span>

### <span data-ttu-id="a4a1c-130">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="a4a1c-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="a4a1c-131">Parameter: webByValue</span><span class="sxs-lookup"><span data-stu-id="a4a1c-131">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="a4a1c-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a4a1c-132">OUTPUTS</span></span>

### <span data-ttu-id="a4a1c-133">Microsoft. Azure. Commands. webapps. Cmdlets. backuprestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="a4a1c-133">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="a4a1c-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="a4a1c-134">NOTES</span></span>

## <span data-ttu-id="a4a1c-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a4a1c-135">RELATED LINKS</span></span>

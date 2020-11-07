---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: fab46f997492c366857c7d13bea38543cca4e91c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658549"
---
# <span data-ttu-id="42406-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="42406-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="42406-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="42406-102">SYNOPSIS</span></span>
<span data-ttu-id="42406-103">Ruft die für eine Web-App verfügbaren Snapshots ab.</span><span class="sxs-lookup"><span data-stu-id="42406-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="42406-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="42406-104">SYNTAX</span></span>

### <span data-ttu-id="42406-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="42406-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42406-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="42406-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42406-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42406-107">DESCRIPTION</span></span>
<span data-ttu-id="42406-108">Das Cmdlet " **Get-AzWebAppSnapshot** " gibt alle Snapshots für eine Web-App zurück.</span><span class="sxs-lookup"><span data-stu-id="42406-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="42406-109">Schnappschüsse sind automatische Sicherungen der Dateien und Einstellungen einer Web-App.</span><span class="sxs-lookup"><span data-stu-id="42406-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="42406-110">Eine Momentaufnahme kann mit dem Cmdlet **Restore-AzWebAppSnapshot** wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="42406-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="42406-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42406-111">EXAMPLES</span></span>

### <span data-ttu-id="42406-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="42406-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="42406-113">Abrufen der Snapshots für eine Web-App mit dem Namen "ConstosoApp" mit einem Slot mit dem Namen "Staging" in der Ressourcengruppe "Standard-Web-westus"</span><span class="sxs-lookup"><span data-stu-id="42406-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="42406-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="42406-114">PARAMETERS</span></span>

### <span data-ttu-id="42406-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42406-115">-DefaultProfile</span></span>
<span data-ttu-id="42406-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="42406-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42406-117">-Name</span><span class="sxs-lookup"><span data-stu-id="42406-117">-Name</span></span>
<span data-ttu-id="42406-118">Der Name der Web-App.</span><span class="sxs-lookup"><span data-stu-id="42406-118">The name of the web app.</span></span>

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

### <span data-ttu-id="42406-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42406-119">-ResourceGroupName</span></span>
<span data-ttu-id="42406-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="42406-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="42406-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="42406-121">-Slot</span></span>
<span data-ttu-id="42406-122">Der Name des Web App-Slots.</span><span class="sxs-lookup"><span data-stu-id="42406-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="42406-123">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="42406-123">-WebApp</span></span>
<span data-ttu-id="42406-124">Das Web App-Objekt</span><span class="sxs-lookup"><span data-stu-id="42406-124">The web app object</span></span>

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

### <span data-ttu-id="42406-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42406-125">CommonParameters</span></span>
<span data-ttu-id="42406-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42406-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42406-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42406-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42406-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="42406-128">INPUTS</span></span>

### <span data-ttu-id="42406-129">System. String</span><span class="sxs-lookup"><span data-stu-id="42406-129">System.String</span></span>

### <span data-ttu-id="42406-130">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="42406-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="42406-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="42406-131">OUTPUTS</span></span>

### <span data-ttu-id="42406-132">Microsoft. Azure. Commands. webapps. Cmdlets. backuprestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="42406-132">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="42406-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="42406-133">NOTES</span></span>

## <span data-ttu-id="42406-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="42406-134">RELATED LINKS</span></span>

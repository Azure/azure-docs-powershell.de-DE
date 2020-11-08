---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: 350f7d5b44f5a1c84f97511a4febb7d967ee2de4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177330"
---
# <span data-ttu-id="1b3b3-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="1b3b3-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="1b3b3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1b3b3-102">SYNOPSIS</span></span>
<span data-ttu-id="1b3b3-103">Ruft die für eine Web-App verfügbaren Snapshots ab.</span><span class="sxs-lookup"><span data-stu-id="1b3b3-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="1b3b3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b3b3-104">SYNTAX</span></span>

### <span data-ttu-id="1b3b3-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="1b3b3-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b3b3-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="1b3b3-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b3b3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1b3b3-107">DESCRIPTION</span></span>
<span data-ttu-id="1b3b3-108">Das Cmdlet " **Get-AzWebAppSnapshot** " gibt alle Snapshots für eine Web-App zurück.</span><span class="sxs-lookup"><span data-stu-id="1b3b3-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="1b3b3-109">Schnappschüsse sind automatische Sicherungen der Dateien und Einstellungen einer Web-App.</span><span class="sxs-lookup"><span data-stu-id="1b3b3-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="1b3b3-110">Eine Momentaufnahme kann mit dem Cmdlet **Restore-AzWebAppSnapshot** wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1b3b3-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="1b3b3-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1b3b3-111">EXAMPLES</span></span>

### <span data-ttu-id="1b3b3-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1b3b3-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="1b3b3-113">Abrufen der Snapshots für eine Web-App mit dem Namen "ContosoApp" mit einem Slot mit dem Namen "Staging" in der Ressourcengruppe "Standard-Web-westus"</span><span class="sxs-lookup"><span data-stu-id="1b3b3-113">Get the snapshots for a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="1b3b3-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b3b3-114">PARAMETERS</span></span>

### <span data-ttu-id="1b3b3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b3b3-115">-DefaultProfile</span></span>
<span data-ttu-id="1b3b3-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1b3b3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b3b3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1b3b3-117">-Name</span></span>
<span data-ttu-id="1b3b3-118">Der Name der Web-App.</span><span class="sxs-lookup"><span data-stu-id="1b3b3-118">The name of the web app.</span></span>

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

### <span data-ttu-id="1b3b3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b3b3-119">-ResourceGroupName</span></span>
<span data-ttu-id="1b3b3-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1b3b3-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="1b3b3-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="1b3b3-121">-Slot</span></span>
<span data-ttu-id="1b3b3-122">Der Name des Web App-Slots.</span><span class="sxs-lookup"><span data-stu-id="1b3b3-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="1b3b3-123">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="1b3b3-123">-UseDisasterRecovery</span></span>
<span data-ttu-id="1b3b3-124">Lesen Sie die Schnappschüsse von einer sekundären Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="1b3b3-124">Read the snapshots from a secondary scale unit.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b3b3-125">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="1b3b3-125">-WebApp</span></span>
<span data-ttu-id="1b3b3-126">Das Web App-Objekt</span><span class="sxs-lookup"><span data-stu-id="1b3b3-126">The web app object</span></span>

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

### <span data-ttu-id="1b3b3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b3b3-127">CommonParameters</span></span>
<span data-ttu-id="1b3b3-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b3b3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b3b3-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b3b3-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b3b3-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1b3b3-130">INPUTS</span></span>

### <span data-ttu-id="1b3b3-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1b3b3-131">System.String</span></span>

### <span data-ttu-id="1b3b3-132">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="1b3b3-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1b3b3-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1b3b3-133">OUTPUTS</span></span>

### <span data-ttu-id="1b3b3-134">Microsoft. Azure. Commands. webapps. Cmdlets. backuprestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="1b3b3-134">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="1b3b3-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="1b3b3-135">NOTES</span></span>

## <span data-ttu-id="1b3b3-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1b3b3-136">RELATED LINKS</span></span>

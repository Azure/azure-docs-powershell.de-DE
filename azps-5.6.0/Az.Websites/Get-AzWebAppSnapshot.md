---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: 14567157501b81ba669061285025ba1631be88d4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932155"
---
# <span data-ttu-id="4ffd5-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="4ffd5-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="4ffd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ffd5-102">SYNOPSIS</span></span>
<span data-ttu-id="4ffd5-103">Ruft die für eine Web-App verfügbaren Momentaufnahmen ab.</span><span class="sxs-lookup"><span data-stu-id="4ffd5-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="4ffd5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ffd5-104">SYNTAX</span></span>

### <span data-ttu-id="4ffd5-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="4ffd5-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ffd5-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="4ffd5-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ffd5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ffd5-107">DESCRIPTION</span></span>
<span data-ttu-id="4ffd5-108">Das **Get-AzWebAppSnapshot-Cmdlet** gibt alle Momentaufnahmen für eine Web-App zurück.</span><span class="sxs-lookup"><span data-stu-id="4ffd5-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="4ffd5-109">Momentaufnahmen sind automatische Sicherungen der Dateien und Einstellungen einer Web App.</span><span class="sxs-lookup"><span data-stu-id="4ffd5-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="4ffd5-110">Eine Momentaufnahme kann mit dem **Cmdlet Restore-AzWebAppSnapshot wiederhergestellt** werden.</span><span class="sxs-lookup"><span data-stu-id="4ffd5-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="4ffd5-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4ffd5-111">EXAMPLES</span></span>

### <span data-ttu-id="4ffd5-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4ffd5-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="4ffd5-113">Holen Sie sich die Momentaufnahmen für eine Web-App namens "ContosoApp" mit einem Slot namens "Staging" in der Ressourcengruppe "Default-Web-WestUS".</span><span class="sxs-lookup"><span data-stu-id="4ffd5-113">Get the snapshots for a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="4ffd5-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4ffd5-114">PARAMETERS</span></span>

### <span data-ttu-id="4ffd5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ffd5-115">-DefaultProfile</span></span>
<span data-ttu-id="4ffd5-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4ffd5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ffd5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4ffd5-117">-Name</span></span>
<span data-ttu-id="4ffd5-118">Der Name der Web App.</span><span class="sxs-lookup"><span data-stu-id="4ffd5-118">The name of the web app.</span></span>

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

### <span data-ttu-id="4ffd5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ffd5-119">-ResourceGroupName</span></span>
<span data-ttu-id="4ffd5-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4ffd5-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="4ffd5-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="4ffd5-121">-Slot</span></span>
<span data-ttu-id="4ffd5-122">Der Name des Web-App-Steckplatzes.</span><span class="sxs-lookup"><span data-stu-id="4ffd5-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="4ffd5-123">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="4ffd5-123">-UseDisasterRecovery</span></span>
<span data-ttu-id="4ffd5-124">Lesen Sie die Momentaufnahmen von einer sekundären Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="4ffd5-124">Read the snapshots from a secondary scale unit.</span></span>

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

### <span data-ttu-id="4ffd5-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="4ffd5-125">-WebApp</span></span>
<span data-ttu-id="4ffd5-126">Das Web App-Objekt</span><span class="sxs-lookup"><span data-stu-id="4ffd5-126">The web app object</span></span>

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

### <span data-ttu-id="4ffd5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ffd5-127">CommonParameters</span></span>
<span data-ttu-id="4ffd5-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ffd5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ffd5-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ffd5-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ffd5-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4ffd5-130">INPUTS</span></span>

### <span data-ttu-id="4ffd5-131">System.String</span><span class="sxs-lookup"><span data-stu-id="4ffd5-131">System.String</span></span>

### <span data-ttu-id="4ffd5-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="4ffd5-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="4ffd5-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4ffd5-133">OUTPUTS</span></span>

### <span data-ttu-id="4ffd5-134">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="4ffd5-134">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="4ffd5-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4ffd5-135">NOTES</span></span>

## <span data-ttu-id="4ffd5-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4ffd5-136">RELATED LINKS</span></span>

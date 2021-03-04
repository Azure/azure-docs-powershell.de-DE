---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
ms.openlocfilehash: f70caa984fde48db6b2d1d147ebf62f544f2ed9f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928803"
---
# <span data-ttu-id="a83e3-101">Get-AzWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="a83e3-101">Get-AzWebAppBackupList</span></span>

## <span data-ttu-id="a83e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a83e3-102">SYNOPSIS</span></span>

## <span data-ttu-id="a83e3-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a83e3-103">SYNTAX</span></span>

### <span data-ttu-id="a83e3-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="a83e3-104">FromResourceName</span></span>
```
Get-AzWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a83e3-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="a83e3-105">FromWebApp</span></span>
```
Get-AzWebAppBackupList [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a83e3-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a83e3-106">DESCRIPTION</span></span>
<span data-ttu-id="a83e3-107">Das **Get-AzWebAppBackupList-Cmdlet** ruft eine Liste der Sicherungen für eine Azure Web App ab.</span><span class="sxs-lookup"><span data-stu-id="a83e3-107">The **Get-AzWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="a83e3-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a83e3-108">EXAMPLES</span></span>

### <span data-ttu-id="a83e3-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a83e3-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="a83e3-110">Dieser Befehl gibt eine Sicherungsliste zurück, die sich auf WebApp WebAppStandard bezieht, die der Ressourcengruppe ContosoResourceGroup zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a83e3-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="a83e3-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a83e3-111">PARAMETERS</span></span>

### <span data-ttu-id="a83e3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a83e3-112">-DefaultProfile</span></span>
<span data-ttu-id="a83e3-113">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a83e3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a83e3-114">-Name</span><span class="sxs-lookup"><span data-stu-id="a83e3-114">-Name</span></span>
<span data-ttu-id="a83e3-115">WebApp-Name</span><span class="sxs-lookup"><span data-stu-id="a83e3-115">WebApp Name</span></span>

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

### <span data-ttu-id="a83e3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a83e3-116">-ResourceGroupName</span></span>
<span data-ttu-id="a83e3-117">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="a83e3-117">Resource Group Name</span></span>

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

### <span data-ttu-id="a83e3-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="a83e3-118">-Slot</span></span>
<span data-ttu-id="a83e3-119">Slotname</span><span class="sxs-lookup"><span data-stu-id="a83e3-119">Slot name</span></span>

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

### <span data-ttu-id="a83e3-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a83e3-120">-WebApp</span></span>
<span data-ttu-id="a83e3-121">Piped WebApp</span><span class="sxs-lookup"><span data-stu-id="a83e3-121">Piped WebApp</span></span>

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

### <span data-ttu-id="a83e3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a83e3-122">CommonParameters</span></span>
<span data-ttu-id="a83e3-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a83e3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a83e3-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a83e3-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a83e3-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a83e3-125">INPUTS</span></span>

### <span data-ttu-id="a83e3-126">System.String</span><span class="sxs-lookup"><span data-stu-id="a83e3-126">System.String</span></span>

### <span data-ttu-id="a83e3-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="a83e3-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a83e3-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a83e3-128">OUTPUTS</span></span>

### <span data-ttu-id="a83e3-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="a83e3-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="a83e3-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a83e3-130">NOTES</span></span>

## <span data-ttu-id="a83e3-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a83e3-131">RELATED LINKS</span></span>

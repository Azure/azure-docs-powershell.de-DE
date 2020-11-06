---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
ms.openlocfilehash: f4005df31746b63b2a45fa2c78f254e2d5f24c59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477541"
---
# <span data-ttu-id="4ea83-101">Get-AzureRmWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="4ea83-101">Get-AzureRmWebAppBackupList</span></span>

## <span data-ttu-id="4ea83-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4ea83-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ea83-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ea83-103">SYNTAX</span></span>

### <span data-ttu-id="4ea83-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="4ea83-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ea83-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="4ea83-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupList [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ea83-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4ea83-106">DESCRIPTION</span></span>
<span data-ttu-id="4ea83-107">Das Cmdlet " **Get-AzureRmWebAppBackupList** " Ruft eine Liste der Sicherungen für eine Azure Web App ab.</span><span class="sxs-lookup"><span data-stu-id="4ea83-107">The **Get-AzureRmWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="4ea83-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4ea83-108">EXAMPLES</span></span>

### <span data-ttu-id="4ea83-109">1:</span><span class="sxs-lookup"><span data-stu-id="4ea83-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="4ea83-110">Dieser Befehl gibt eine Sicherungsliste zurück, die sich auf die WebAppStandard der Ressourcengruppe ContosoResourceGroup bezieht.</span><span class="sxs-lookup"><span data-stu-id="4ea83-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="4ea83-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ea83-111">PARAMETERS</span></span>

### <span data-ttu-id="4ea83-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ea83-112">-DefaultProfile</span></span>
<span data-ttu-id="4ea83-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4ea83-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ea83-114">-Name</span><span class="sxs-lookup"><span data-stu-id="4ea83-114">-Name</span></span>
<span data-ttu-id="4ea83-115">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="4ea83-115">WebApp Name</span></span>

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

### <span data-ttu-id="4ea83-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ea83-116">-ResourceGroupName</span></span>
<span data-ttu-id="4ea83-117">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="4ea83-117">Resource Group Name</span></span>

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

### <span data-ttu-id="4ea83-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="4ea83-118">-Slot</span></span>
<span data-ttu-id="4ea83-119">Name des Steckplatzes</span><span class="sxs-lookup"><span data-stu-id="4ea83-119">Slot name</span></span>

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

### <span data-ttu-id="4ea83-120">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="4ea83-120">-WebApp</span></span>
<span data-ttu-id="4ea83-121">Pipelining</span><span class="sxs-lookup"><span data-stu-id="4ea83-121">Piped WebApp</span></span>

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

### <span data-ttu-id="4ea83-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ea83-122">CommonParameters</span></span>
<span data-ttu-id="4ea83-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ea83-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ea83-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ea83-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ea83-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4ea83-125">INPUTS</span></span>

### <span data-ttu-id="4ea83-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4ea83-126">System.String</span></span>

### <span data-ttu-id="4ea83-127">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="4ea83-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="4ea83-128">Parameter: webByValue</span><span class="sxs-lookup"><span data-stu-id="4ea83-128">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="4ea83-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4ea83-129">OUTPUTS</span></span>

### <span data-ttu-id="4ea83-130">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="4ea83-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="4ea83-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="4ea83-131">NOTES</span></span>

## <span data-ttu-id="4ea83-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4ea83-132">RELATED LINKS</span></span>

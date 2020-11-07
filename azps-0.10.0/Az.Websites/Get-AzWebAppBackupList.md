---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackupList.md
ms.openlocfilehash: 057bebde5eada143c9ee00260a1406fdceae9436
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842791"
---
# <span data-ttu-id="dd356-101">Get-AzWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="dd356-101">Get-AzWebAppBackupList</span></span>

## <span data-ttu-id="dd356-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dd356-102">SYNOPSIS</span></span>

## <span data-ttu-id="dd356-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd356-103">SYNTAX</span></span>

### <span data-ttu-id="dd356-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="dd356-104">FromResourceName</span></span>
```
Get-AzWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd356-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="dd356-105">FromWebApp</span></span>
```
Get-AzWebAppBackupList [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd356-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd356-106">DESCRIPTION</span></span>
<span data-ttu-id="dd356-107">Das Cmdlet " **Get-AzWebAppBackupList** " Ruft eine Liste der Sicherungen für eine Azure Web App ab.</span><span class="sxs-lookup"><span data-stu-id="dd356-107">The **Get-AzWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="dd356-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd356-108">EXAMPLES</span></span>

### <span data-ttu-id="dd356-109">1:</span><span class="sxs-lookup"><span data-stu-id="dd356-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="dd356-110">Dieser Befehl gibt eine Sicherungsliste zurück, die sich auf die WebAppStandard der Ressourcengruppe ContosoResourceGroup bezieht.</span><span class="sxs-lookup"><span data-stu-id="dd356-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="dd356-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd356-111">PARAMETERS</span></span>

### <span data-ttu-id="dd356-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd356-112">-DefaultProfile</span></span>
<span data-ttu-id="dd356-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dd356-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd356-114">-Name</span><span class="sxs-lookup"><span data-stu-id="dd356-114">-Name</span></span>
<span data-ttu-id="dd356-115">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="dd356-115">WebApp Name</span></span>

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

### <span data-ttu-id="dd356-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd356-116">-ResourceGroupName</span></span>
<span data-ttu-id="dd356-117">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="dd356-117">Resource Group Name</span></span>

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

### <span data-ttu-id="dd356-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="dd356-118">-Slot</span></span>
<span data-ttu-id="dd356-119">Name des Steckplatzes</span><span class="sxs-lookup"><span data-stu-id="dd356-119">Slot name</span></span>

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

### <span data-ttu-id="dd356-120">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="dd356-120">-WebApp</span></span>
<span data-ttu-id="dd356-121">Pipelining</span><span class="sxs-lookup"><span data-stu-id="dd356-121">Piped WebApp</span></span>

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

### <span data-ttu-id="dd356-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd356-122">CommonParameters</span></span>
<span data-ttu-id="dd356-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd356-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd356-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd356-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd356-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dd356-125">INPUTS</span></span>

### <span data-ttu-id="dd356-126">Website</span><span class="sxs-lookup"><span data-stu-id="dd356-126">Site</span></span>
<span data-ttu-id="dd356-127">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="dd356-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="dd356-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dd356-128">OUTPUTS</span></span>

### <span data-ttu-id="dd356-129">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackup []</span><span class="sxs-lookup"><span data-stu-id="dd356-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup[]</span></span>

## <span data-ttu-id="dd356-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="dd356-130">NOTES</span></span>

## <span data-ttu-id="dd356-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dd356-131">RELATED LINKS</span></span>


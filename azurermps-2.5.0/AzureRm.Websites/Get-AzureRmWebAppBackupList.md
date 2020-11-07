---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackuplist
schema: 2.0.0
ms.openlocfilehash: ef409c62d56a95d36f1e7c9a02018b281c00e3c9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848615"
---
# <span data-ttu-id="9094e-101">Get-AzureRmWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="9094e-101">Get-AzureRmWebAppBackupList</span></span>

## <span data-ttu-id="9094e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9094e-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9094e-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="9094e-103">SYNTAX</span></span>

### <span data-ttu-id="9094e-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="9094e-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9094e-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="9094e-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupList [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9094e-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9094e-106">DESCRIPTION</span></span>
<span data-ttu-id="9094e-107">Das Cmdlet " **Get-AzureRmWebAppBackupList** " Ruft eine Liste der Sicherungen für eine Azure Web App ab.</span><span class="sxs-lookup"><span data-stu-id="9094e-107">The **Get-AzureRmWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="9094e-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9094e-108">EXAMPLES</span></span>

### <span data-ttu-id="9094e-109">1:</span><span class="sxs-lookup"><span data-stu-id="9094e-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="9094e-110">Dieser Befehl gibt eine Sicherungsliste zurück, die sich auf die WebAppStandard der Ressourcengruppe ContosoResourceGroup bezieht.</span><span class="sxs-lookup"><span data-stu-id="9094e-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="9094e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9094e-111">PARAMETERS</span></span>

### <span data-ttu-id="9094e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9094e-112">-DefaultProfile</span></span>
<span data-ttu-id="9094e-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9094e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9094e-114">-Name</span><span class="sxs-lookup"><span data-stu-id="9094e-114">-Name</span></span>
<span data-ttu-id="9094e-115">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="9094e-115">WebApp Name</span></span>

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

### <span data-ttu-id="9094e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9094e-116">-ResourceGroupName</span></span>
<span data-ttu-id="9094e-117">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="9094e-117">Resource Group Name</span></span>

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

### <span data-ttu-id="9094e-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="9094e-118">-Slot</span></span>
<span data-ttu-id="9094e-119">Name des Steckplatzes</span><span class="sxs-lookup"><span data-stu-id="9094e-119">Slot name</span></span>

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

### <span data-ttu-id="9094e-120">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="9094e-120">-WebApp</span></span>
<span data-ttu-id="9094e-121">Pipelining</span><span class="sxs-lookup"><span data-stu-id="9094e-121">Piped WebApp</span></span>

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

### <span data-ttu-id="9094e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9094e-122">CommonParameters</span></span>
<span data-ttu-id="9094e-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9094e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9094e-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9094e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9094e-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9094e-125">INPUTS</span></span>

### <span data-ttu-id="9094e-126">Website</span><span class="sxs-lookup"><span data-stu-id="9094e-126">Site</span></span>
<span data-ttu-id="9094e-127">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="9094e-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="9094e-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9094e-128">OUTPUTS</span></span>

### <span data-ttu-id="9094e-129">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackup []</span><span class="sxs-lookup"><span data-stu-id="9094e-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup[]</span></span>

## <span data-ttu-id="9094e-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="9094e-130">NOTES</span></span>

## <span data-ttu-id="9094e-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9094e-131">RELATED LINKS</span></span>


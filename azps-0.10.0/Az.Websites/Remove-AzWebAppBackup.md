---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/remove-Azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebAppBackup.md
ms.openlocfilehash: d8c25931e5eeae035f319c36698369b865500b9a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842720"
---
# <span data-ttu-id="8292f-101">Remove-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="8292f-101">Remove-AzWebAppBackup</span></span>

## <span data-ttu-id="8292f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8292f-102">SYNOPSIS</span></span>

## <span data-ttu-id="8292f-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="8292f-103">SYNTAX</span></span>

### <span data-ttu-id="8292f-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="8292f-104">FromResourceName</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8292f-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="8292f-105">FromWebApp</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8292f-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8292f-106">DESCRIPTION</span></span>
<span data-ttu-id="8292f-107">Das Cmdlet **Remove-AzWebAppBackup** entfernt die angegebene Sicherung einer Azure Web-App.</span><span class="sxs-lookup"><span data-stu-id="8292f-107">The **Remove-AzWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="8292f-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8292f-108">EXAMPLES</span></span>

### <span data-ttu-id="8292f-109">1:</span><span class="sxs-lookup"><span data-stu-id="8292f-109">1:</span></span>
```
PS C:\>Remove-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="8292f-110">Mit diesem Befehl wird die Sicherung mit der ID "12345" aus der Web-App mit dem Namen "WebAppStandard" entfernt, die zum Standard-Web-westus der Ressourcengruppe gehört.</span><span class="sxs-lookup"><span data-stu-id="8292f-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="8292f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="8292f-111">PARAMETERS</span></span>

### <span data-ttu-id="8292f-112">-Backup-Nr.</span><span class="sxs-lookup"><span data-stu-id="8292f-112">-BackupId</span></span>
<span data-ttu-id="8292f-113">Sicherungs-ID</span><span class="sxs-lookup"><span data-stu-id="8292f-113">Backup Id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8292f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8292f-114">-DefaultProfile</span></span>
<span data-ttu-id="8292f-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8292f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8292f-116">-Name</span><span class="sxs-lookup"><span data-stu-id="8292f-116">-Name</span></span>
<span data-ttu-id="8292f-117">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="8292f-117">WebApp Name</span></span>

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

### <span data-ttu-id="8292f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8292f-118">-ResourceGroupName</span></span>
<span data-ttu-id="8292f-119">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="8292f-119">Resource Group Name</span></span>

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

### <span data-ttu-id="8292f-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="8292f-120">-Slot</span></span>
<span data-ttu-id="8292f-121">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="8292f-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="8292f-122">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="8292f-122">-WebApp</span></span>
<span data-ttu-id="8292f-123">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="8292f-123">WebApp Object</span></span>

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

### <span data-ttu-id="8292f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8292f-124">CommonParameters</span></span>
<span data-ttu-id="8292f-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8292f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8292f-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8292f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8292f-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8292f-127">INPUTS</span></span>

### <span data-ttu-id="8292f-128">Website</span><span class="sxs-lookup"><span data-stu-id="8292f-128">Site</span></span>
<span data-ttu-id="8292f-129">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="8292f-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="8292f-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8292f-130">OUTPUTS</span></span>

### <span data-ttu-id="8292f-131">Microsoft. Azure. Management. Websites. Models. BackupItem</span><span class="sxs-lookup"><span data-stu-id="8292f-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="8292f-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="8292f-132">NOTES</span></span>

## <span data-ttu-id="8292f-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8292f-133">RELATED LINKS</span></span>


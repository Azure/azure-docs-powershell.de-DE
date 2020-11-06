---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppBackup.md
ms.openlocfilehash: ba7255c41b5851b1f34b2ff7a1523c691925bae0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504662"
---
# <span data-ttu-id="2096d-101">Remove-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="2096d-101">Remove-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="2096d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2096d-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2096d-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="2096d-103">SYNTAX</span></span>

### <span data-ttu-id="2096d-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="2096d-104">FromResourceName</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2096d-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="2096d-105">FromWebApp</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2096d-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2096d-106">DESCRIPTION</span></span>
<span data-ttu-id="2096d-107">Das Cmdlet **Remove-AzureRmWebAppBackup** entfernt die angegebene Sicherung einer Azure Web-App.</span><span class="sxs-lookup"><span data-stu-id="2096d-107">The **Remove-AzureRmWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="2096d-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2096d-108">EXAMPLES</span></span>

### <span data-ttu-id="2096d-109">1:</span><span class="sxs-lookup"><span data-stu-id="2096d-109">1:</span></span>
```
PS C:\>Remove-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="2096d-110">Mit diesem Befehl wird die Sicherung mit der ID "12345" aus der Web-App mit dem Namen "WebAppStandard" entfernt, die zum Standard-Web-westus der Ressourcengruppe gehört.</span><span class="sxs-lookup"><span data-stu-id="2096d-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="2096d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2096d-111">PARAMETERS</span></span>

### <span data-ttu-id="2096d-112">-Backup-Nr.</span><span class="sxs-lookup"><span data-stu-id="2096d-112">-BackupId</span></span>
<span data-ttu-id="2096d-113">Sicherungs-ID</span><span class="sxs-lookup"><span data-stu-id="2096d-113">Backup Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2096d-114">-Name</span><span class="sxs-lookup"><span data-stu-id="2096d-114">-Name</span></span>
<span data-ttu-id="2096d-115">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="2096d-115">WebApp Name</span></span>

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

### <span data-ttu-id="2096d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2096d-116">-ResourceGroupName</span></span>
<span data-ttu-id="2096d-117">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="2096d-117">Resource Group Name</span></span>

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

### <span data-ttu-id="2096d-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="2096d-118">-Slot</span></span>
<span data-ttu-id="2096d-119">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="2096d-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="2096d-120">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="2096d-120">-WebApp</span></span>
<span data-ttu-id="2096d-121">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="2096d-121">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2096d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2096d-122">-DefaultProfile</span></span>
<span data-ttu-id="2096d-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2096d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2096d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2096d-124">CommonParameters</span></span>
<span data-ttu-id="2096d-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2096d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2096d-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2096d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2096d-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2096d-127">INPUTS</span></span>

### <span data-ttu-id="2096d-128">Website</span><span class="sxs-lookup"><span data-stu-id="2096d-128">Site</span></span>
<span data-ttu-id="2096d-129">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="2096d-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="2096d-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2096d-130">OUTPUTS</span></span>

### <span data-ttu-id="2096d-131">Microsoft. Azure. Management. Websites. Models. BackupItem</span><span class="sxs-lookup"><span data-stu-id="2096d-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="2096d-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="2096d-132">NOTES</span></span>

## <span data-ttu-id="2096d-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2096d-133">RELATED LINKS</span></span>


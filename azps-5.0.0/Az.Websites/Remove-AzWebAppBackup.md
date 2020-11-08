---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
ms.openlocfilehash: e50c711e730f3af79ce5d8825e6beeee9b663e00
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179462"
---
# <span data-ttu-id="80e46-101">Remove-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="80e46-101">Remove-AzWebAppBackup</span></span>

## <span data-ttu-id="80e46-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="80e46-102">SYNOPSIS</span></span>

## <span data-ttu-id="80e46-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="80e46-103">SYNTAX</span></span>

### <span data-ttu-id="80e46-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="80e46-104">FromResourceName</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80e46-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="80e46-105">FromWebApp</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="80e46-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80e46-106">DESCRIPTION</span></span>
<span data-ttu-id="80e46-107">Das Cmdlet **Remove-AzWebAppBackup** entfernt die angegebene Sicherung einer Azure Web-App.</span><span class="sxs-lookup"><span data-stu-id="80e46-107">The **Remove-AzWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="80e46-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="80e46-108">EXAMPLES</span></span>

### <span data-ttu-id="80e46-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="80e46-109">Example 1</span></span>
```powershell
PS C:\>Remove-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="80e46-110">Mit diesem Befehl wird die Sicherung mit der ID "12345" aus der Web-App mit dem Namen "WebAppStandard" entfernt, die zum Standard-Web-westus der Ressourcengruppe gehört.</span><span class="sxs-lookup"><span data-stu-id="80e46-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="80e46-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="80e46-111">PARAMETERS</span></span>

### <span data-ttu-id="80e46-112">-Backup-Nr.</span><span class="sxs-lookup"><span data-stu-id="80e46-112">-BackupId</span></span>
<span data-ttu-id="80e46-113">Sicherungs-ID</span><span class="sxs-lookup"><span data-stu-id="80e46-113">Backup Id</span></span>

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

### <span data-ttu-id="80e46-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80e46-114">-DefaultProfile</span></span>
<span data-ttu-id="80e46-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="80e46-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80e46-116">-Name</span><span class="sxs-lookup"><span data-stu-id="80e46-116">-Name</span></span>
<span data-ttu-id="80e46-117">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="80e46-117">WebApp Name</span></span>

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

### <span data-ttu-id="80e46-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80e46-118">-ResourceGroupName</span></span>
<span data-ttu-id="80e46-119">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="80e46-119">Resource Group Name</span></span>

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

### <span data-ttu-id="80e46-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="80e46-120">-Slot</span></span>
<span data-ttu-id="80e46-121">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="80e46-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="80e46-122">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="80e46-122">-WebApp</span></span>
<span data-ttu-id="80e46-123">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="80e46-123">WebApp Object</span></span>

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

### <span data-ttu-id="80e46-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80e46-124">CommonParameters</span></span>
<span data-ttu-id="80e46-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80e46-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80e46-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80e46-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80e46-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="80e46-127">INPUTS</span></span>

### <span data-ttu-id="80e46-128">System. String</span><span class="sxs-lookup"><span data-stu-id="80e46-128">System.String</span></span>

### <span data-ttu-id="80e46-129">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="80e46-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="80e46-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="80e46-130">OUTPUTS</span></span>

### <span data-ttu-id="80e46-131">Microsoft. Azure. Management. Websites. Models. BackupItem</span><span class="sxs-lookup"><span data-stu-id="80e46-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="80e46-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="80e46-132">NOTES</span></span>

## <span data-ttu-id="80e46-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="80e46-133">RELATED LINKS</span></span>

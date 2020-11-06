---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebAppSlot.md
ms.openlocfilehash: 2e6130b93a3c549ca84c2cb0a6a336f6afb177b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495566"
---
# <span data-ttu-id="225db-101">Stop-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="225db-101">Stop-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="225db-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="225db-102">SYNOPSIS</span></span>
<span data-ttu-id="225db-103">Beendet einen Azure Web App-Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="225db-103">Stops an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="225db-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="225db-104">SYNTAX</span></span>

### <span data-ttu-id="225db-105">S1</span><span class="sxs-lookup"><span data-stu-id="225db-105">S1</span></span>
```
Stop-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="225db-106">S2</span><span class="sxs-lookup"><span data-stu-id="225db-106">S2</span></span>
```
Stop-AzureRmWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="225db-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="225db-107">DESCRIPTION</span></span>
<span data-ttu-id="225db-108">Das Cmdlet **Stop-AzureRmWebAppSlot** beendet einen Azure Web App-Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="225db-108">The **Stop-AzureRmWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="225db-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="225db-109">EXAMPLES</span></span>

### <span data-ttu-id="225db-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="225db-110">Example 1</span></span>
```
PS C:\>Stop-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="225db-111">Mit diesem Befehl wird der Slot Slot001 in Bezug auf die Web-App mit dem Namen ContosoWebApp, die zu der Ressourcengruppe Default-Web-westus gehört, beendet.</span><span class="sxs-lookup"><span data-stu-id="225db-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="225db-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="225db-112">PARAMETERS</span></span>

### <span data-ttu-id="225db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="225db-113">-DefaultProfile</span></span>
<span data-ttu-id="225db-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="225db-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="225db-115">-Name</span><span class="sxs-lookup"><span data-stu-id="225db-115">-Name</span></span>
<span data-ttu-id="225db-116">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="225db-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="225db-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="225db-117">-ResourceGroupName</span></span>
<span data-ttu-id="225db-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="225db-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225db-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="225db-119">-Slot</span></span>
<span data-ttu-id="225db-120">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="225db-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225db-121">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="225db-121">-WebApp</span></span>
<span data-ttu-id="225db-122">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="225db-122">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="225db-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="225db-123">CommonParameters</span></span>
<span data-ttu-id="225db-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="225db-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="225db-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="225db-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="225db-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="225db-126">INPUTS</span></span>

### <span data-ttu-id="225db-127">System. String</span><span class="sxs-lookup"><span data-stu-id="225db-127">System.String</span></span>

### <span data-ttu-id="225db-128">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="225db-128">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="225db-129">Parameter: webByValue</span><span class="sxs-lookup"><span data-stu-id="225db-129">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="225db-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="225db-130">OUTPUTS</span></span>

### <span data-ttu-id="225db-131">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="225db-131">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="225db-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="225db-132">NOTES</span></span>

## <span data-ttu-id="225db-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="225db-133">RELATED LINKS</span></span>

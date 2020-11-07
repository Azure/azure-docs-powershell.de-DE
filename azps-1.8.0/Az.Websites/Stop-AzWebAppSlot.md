---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
ms.openlocfilehash: 455a1735df128ee84d99adb6461c602a7b1dbbdf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658490"
---
# <span data-ttu-id="b9f7c-101">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b9f7c-101">Stop-AzWebAppSlot</span></span>

## <span data-ttu-id="b9f7c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b9f7c-102">SYNOPSIS</span></span>
<span data-ttu-id="b9f7c-103">Beendet einen Azure Web App-Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="b9f7c-103">Stops an Azure Web App slot.</span></span>

## <span data-ttu-id="b9f7c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9f7c-104">SYNTAX</span></span>

### <span data-ttu-id="b9f7c-105">S1</span><span class="sxs-lookup"><span data-stu-id="b9f7c-105">S1</span></span>
```
Stop-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9f7c-106">S2</span><span class="sxs-lookup"><span data-stu-id="b9f7c-106">S2</span></span>
```
Stop-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9f7c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b9f7c-107">DESCRIPTION</span></span>
<span data-ttu-id="b9f7c-108">Das Cmdlet **Stop-AzWebAppSlot** beendet einen Azure Web App-Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="b9f7c-108">The **Stop-AzWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="b9f7c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b9f7c-109">EXAMPLES</span></span>

### <span data-ttu-id="b9f7c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b9f7c-110">Example 1</span></span>
```
PS C:\>Stop-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="b9f7c-111">Mit diesem Befehl wird der Slot Slot001 in Bezug auf die Web-App mit dem Namen ContosoWebApp, die zu der Ressourcengruppe Default-Web-westus gehört, beendet.</span><span class="sxs-lookup"><span data-stu-id="b9f7c-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="b9f7c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9f7c-112">PARAMETERS</span></span>

### <span data-ttu-id="b9f7c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9f7c-113">-DefaultProfile</span></span>
<span data-ttu-id="b9f7c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b9f7c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9f7c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b9f7c-115">-Name</span></span>
<span data-ttu-id="b9f7c-116">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="b9f7c-116">WebApp Name</span></span>

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

### <span data-ttu-id="b9f7c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9f7c-117">-ResourceGroupName</span></span>
<span data-ttu-id="b9f7c-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="b9f7c-118">Resource Group Name</span></span>

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

### <span data-ttu-id="b9f7c-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="b9f7c-119">-Slot</span></span>
<span data-ttu-id="b9f7c-120">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="b9f7c-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="b9f7c-121">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="b9f7c-121">-WebApp</span></span>
<span data-ttu-id="b9f7c-122">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="b9f7c-122">WebApp Object</span></span>

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

### <span data-ttu-id="b9f7c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9f7c-123">CommonParameters</span></span>
<span data-ttu-id="b9f7c-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9f7c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9f7c-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9f7c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9f7c-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b9f7c-126">INPUTS</span></span>

### <span data-ttu-id="b9f7c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b9f7c-127">System.String</span></span>

### <span data-ttu-id="b9f7c-128">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="b9f7c-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b9f7c-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b9f7c-129">OUTPUTS</span></span>

### <span data-ttu-id="b9f7c-130">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="b9f7c-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b9f7c-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="b9f7c-131">NOTES</span></span>

## <span data-ttu-id="b9f7c-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b9f7c-132">RELATED LINKS</span></span>

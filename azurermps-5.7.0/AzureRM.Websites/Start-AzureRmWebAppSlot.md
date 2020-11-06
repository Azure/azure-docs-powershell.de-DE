---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/start-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebAppSlot.md
ms.openlocfilehash: e9b0fa9f492c64f86668688d12171795735a46dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476430"
---
# <span data-ttu-id="33ae7-101">Start-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="33ae7-101">Start-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="33ae7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="33ae7-102">SYNOPSIS</span></span>
<span data-ttu-id="33ae7-103">Startet einen Azure Web App-Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="33ae7-103">Starts an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33ae7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="33ae7-104">SYNTAX</span></span>

### <span data-ttu-id="33ae7-105">S1</span><span class="sxs-lookup"><span data-stu-id="33ae7-105">S1</span></span>
```
Start-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33ae7-106">S2</span><span class="sxs-lookup"><span data-stu-id="33ae7-106">S2</span></span>
```
Start-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33ae7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="33ae7-107">DESCRIPTION</span></span>
<span data-ttu-id="33ae7-108">Mit dem **Start-AzureRmWebAppSlot-** Cmdlet wird ein Azure Web App-Steckplatz gestartet.</span><span class="sxs-lookup"><span data-stu-id="33ae7-108">The **Start-AzureRmWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="33ae7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="33ae7-109">EXAMPLES</span></span>

### <span data-ttu-id="33ae7-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="33ae7-110">Example 1</span></span>
```
PS C:\>Start-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="33ae7-111">Mit diesem Befehl wird der Slot mit dem Namen Slot001 in Bezug auf die Web-App mit dem Namen ContosoWebApp gestartet, die zu der Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="33ae7-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="33ae7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="33ae7-112">PARAMETERS</span></span>

### <span data-ttu-id="33ae7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33ae7-113">-DefaultProfile</span></span>
<span data-ttu-id="33ae7-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="33ae7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33ae7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="33ae7-115">-Name</span></span>
<span data-ttu-id="33ae7-116">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="33ae7-116">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33ae7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33ae7-117">-ResourceGroupName</span></span>
<span data-ttu-id="33ae7-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="33ae7-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ae7-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="33ae7-119">-Slot</span></span>
<span data-ttu-id="33ae7-120">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="33ae7-120">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ae7-121">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="33ae7-121">-WebApp</span></span>
<span data-ttu-id="33ae7-122">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="33ae7-122">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33ae7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33ae7-123">CommonParameters</span></span>
<span data-ttu-id="33ae7-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33ae7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33ae7-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33ae7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33ae7-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="33ae7-126">INPUTS</span></span>

### <span data-ttu-id="33ae7-127">Website</span><span class="sxs-lookup"><span data-stu-id="33ae7-127">Site</span></span>
<span data-ttu-id="33ae7-128">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="33ae7-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="33ae7-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="33ae7-129">OUTPUTS</span></span>

## <span data-ttu-id="33ae7-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="33ae7-130">NOTES</span></span>

## <span data-ttu-id="33ae7-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="33ae7-131">RELATED LINKS</span></span>

[<span data-ttu-id="33ae7-132">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="33ae7-132">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="33ae7-133">Neu – AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="33ae7-133">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="33ae7-134">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="33ae7-134">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="33ae7-135">Neustart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="33ae7-135">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="33ae7-136">Satz-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="33ae7-136">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="33ae7-137">Stopp-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="33ae7-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="33ae7-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="33ae7-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

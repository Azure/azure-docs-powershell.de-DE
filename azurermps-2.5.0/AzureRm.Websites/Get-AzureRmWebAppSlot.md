---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: 9ac20046317fa7d070e69284696293e1f66ed486
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848603"
---
# <span data-ttu-id="9e147-101">Get-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9e147-101">Get-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="9e147-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9e147-102">SYNOPSIS</span></span>
<span data-ttu-id="9e147-103">Ruft einen Azure Web App-Steckplatz ab.</span><span class="sxs-lookup"><span data-stu-id="9e147-103">Gets an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e147-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e147-104">SYNTAX</span></span>

### <span data-ttu-id="9e147-105">S1</span><span class="sxs-lookup"><span data-stu-id="9e147-105">S1</span></span>
```
Get-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e147-106">S2</span><span class="sxs-lookup"><span data-stu-id="9e147-106">S2</span></span>
```
Get-AzureRmWebAppSlot [[-Slot] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e147-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e147-107">DESCRIPTION</span></span>
<span data-ttu-id="9e147-108">Das Cmdlet " **Get-AzureRmWebAppSlot** " Ruft Informationen zu einem Azure Web App-Slot ab.</span><span class="sxs-lookup"><span data-stu-id="9e147-108">The **Get-AzureRmWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="9e147-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9e147-109">EXAMPLES</span></span>

### <span data-ttu-id="9e147-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9e147-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="9e147-111">Dieser Befehl ruft den Steckplatz mit dem Namen Slot001 aus der Web-App mit dem Namen WebAppStandard ab, die zu der Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="9e147-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="9e147-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e147-112">PARAMETERS</span></span>

### <span data-ttu-id="9e147-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e147-113">-DefaultProfile</span></span>
<span data-ttu-id="9e147-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9e147-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e147-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9e147-115">-Name</span></span>
<span data-ttu-id="9e147-116">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="9e147-116">WebApp Name</span></span>

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

### <span data-ttu-id="9e147-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e147-117">-ResourceGroupName</span></span>
<span data-ttu-id="9e147-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="9e147-118">Resource Group Name</span></span>

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

### <span data-ttu-id="9e147-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="9e147-119">-Slot</span></span>
<span data-ttu-id="9e147-120">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="9e147-120">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e147-121">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="9e147-121">-WebApp</span></span>
<span data-ttu-id="9e147-122">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="9e147-122">WebApp Object</span></span>

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

### <span data-ttu-id="9e147-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e147-123">CommonParameters</span></span>
<span data-ttu-id="9e147-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e147-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e147-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e147-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e147-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9e147-126">INPUTS</span></span>

### <span data-ttu-id="9e147-127">Website</span><span class="sxs-lookup"><span data-stu-id="9e147-127">Site</span></span>
<span data-ttu-id="9e147-128">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="9e147-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="9e147-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9e147-129">OUTPUTS</span></span>

## <span data-ttu-id="9e147-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="9e147-130">NOTES</span></span>

## <span data-ttu-id="9e147-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9e147-131">RELATED LINKS</span></span>

[<span data-ttu-id="9e147-132">Neu – AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9e147-132">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="9e147-133">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9e147-133">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="9e147-134">Neustart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9e147-134">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="9e147-135">Satz-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9e147-135">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="9e147-136">Anfang-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9e147-136">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="9e147-137">Stopp-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9e147-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="9e147-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9e147-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

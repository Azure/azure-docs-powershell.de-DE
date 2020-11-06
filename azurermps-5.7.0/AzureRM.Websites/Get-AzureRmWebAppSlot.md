---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlot.md
ms.openlocfilehash: b22dcb6518aa42104a44207e85d02dd7bab914bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478125"
---
# <span data-ttu-id="c8bcd-101">Get-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c8bcd-101">Get-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="c8bcd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c8bcd-102">SYNOPSIS</span></span>
<span data-ttu-id="c8bcd-103">Ruft einen Azure Web App-Steckplatz ab.</span><span class="sxs-lookup"><span data-stu-id="c8bcd-103">Gets an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8bcd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8bcd-104">SYNTAX</span></span>

### <span data-ttu-id="c8bcd-105">S1</span><span class="sxs-lookup"><span data-stu-id="c8bcd-105">S1</span></span>
```
Get-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8bcd-106">S2</span><span class="sxs-lookup"><span data-stu-id="c8bcd-106">S2</span></span>
```
Get-AzureRmWebAppSlot [[-Slot] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c8bcd-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8bcd-107">DESCRIPTION</span></span>
<span data-ttu-id="c8bcd-108">Das Cmdlet " **Get-AzureRmWebAppSlot** " Ruft Informationen zu einem Azure Web App-Slot ab.</span><span class="sxs-lookup"><span data-stu-id="c8bcd-108">The **Get-AzureRmWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="c8bcd-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c8bcd-109">EXAMPLES</span></span>

### <span data-ttu-id="c8bcd-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c8bcd-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="c8bcd-111">Dieser Befehl ruft den Steckplatz mit dem Namen Slot001 aus der Web-App mit dem Namen WebAppStandard ab, die zu der Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="c8bcd-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="c8bcd-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8bcd-112">PARAMETERS</span></span>

### <span data-ttu-id="c8bcd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8bcd-113">-DefaultProfile</span></span>
<span data-ttu-id="c8bcd-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c8bcd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8bcd-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c8bcd-115">-Name</span></span>
<span data-ttu-id="c8bcd-116">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="c8bcd-116">WebApp Name</span></span>

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

### <span data-ttu-id="c8bcd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8bcd-117">-ResourceGroupName</span></span>
<span data-ttu-id="c8bcd-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="c8bcd-118">Resource Group Name</span></span>

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

### <span data-ttu-id="c8bcd-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="c8bcd-119">-Slot</span></span>
<span data-ttu-id="c8bcd-120">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="c8bcd-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="c8bcd-121">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="c8bcd-121">-WebApp</span></span>
<span data-ttu-id="c8bcd-122">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="c8bcd-122">WebApp Object</span></span>

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

### <span data-ttu-id="c8bcd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8bcd-123">CommonParameters</span></span>
<span data-ttu-id="c8bcd-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8bcd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8bcd-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8bcd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8bcd-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c8bcd-126">INPUTS</span></span>

### <span data-ttu-id="c8bcd-127">Website</span><span class="sxs-lookup"><span data-stu-id="c8bcd-127">Site</span></span>
<span data-ttu-id="c8bcd-128">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c8bcd-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="c8bcd-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c8bcd-129">OUTPUTS</span></span>

## <span data-ttu-id="c8bcd-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="c8bcd-130">NOTES</span></span>

## <span data-ttu-id="c8bcd-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c8bcd-131">RELATED LINKS</span></span>

[<span data-ttu-id="c8bcd-132">Neu – AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c8bcd-132">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="c8bcd-133">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c8bcd-133">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="c8bcd-134">Neustart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c8bcd-134">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="c8bcd-135">Satz-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c8bcd-135">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="c8bcd-136">Anfang-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c8bcd-136">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="c8bcd-137">Stopp-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c8bcd-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="c8bcd-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c8bcd-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

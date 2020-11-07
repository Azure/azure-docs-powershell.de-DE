---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslotconfigname
schema: 2.0.0
ms.openlocfilehash: 39c3ce693a1ee17a5b547c027ab9165388fe10f2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849871"
---
# <span data-ttu-id="350b1-101">Set-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="350b1-101">Set-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="350b1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="350b1-102">SYNOPSIS</span></span>
<span data-ttu-id="350b1-103">Einrichten von config-Namen für Web App-Steckplätze</span><span class="sxs-lookup"><span data-stu-id="350b1-103">Set Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="350b1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="350b1-104">SYNTAX</span></span>

### <span data-ttu-id="350b1-105">S1</span><span class="sxs-lookup"><span data-stu-id="350b1-105">S1</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="350b1-106">S2</span><span class="sxs-lookup"><span data-stu-id="350b1-106">S2</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="350b1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="350b1-107">DESCRIPTION</span></span>
<span data-ttu-id="350b1-108">Das Cmdlet " **Satz-AzureRmWebAppSlotConfigName** " kennzeichnet App-Einstellungen und Verbindungszeichenfolgen als Steckplatz Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="350b1-108">The **Set-AzureRmWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="350b1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="350b1-109">EXAMPLES</span></span>

### <span data-ttu-id="350b1-110">1:</span><span class="sxs-lookup"><span data-stu-id="350b1-110">1:</span></span>
```
PS C:\> Set-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="350b1-111">Dieser Befehl entfernt alle App-Einstellungen und Verbindungszeichenfolgen für Web-App-ContosoWebApp, die mit der Ressourcengruppe Standard verknüpft sind – Web-westus</span><span class="sxs-lookup"><span data-stu-id="350b1-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="350b1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="350b1-112">PARAMETERS</span></span>

### <span data-ttu-id="350b1-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="350b1-113">-AppSettingNames</span></span>
<span data-ttu-id="350b1-114">Zeichenfolgen Array für App-Einstellungsnamen</span><span class="sxs-lookup"><span data-stu-id="350b1-114">App Settings Names String Array</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="350b1-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="350b1-115">-ConnectionStringNames</span></span>
<span data-ttu-id="350b1-116">Zeichenfolgen Array für Verbindungszeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="350b1-116">Connection String Names String Array</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="350b1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="350b1-117">-DefaultProfile</span></span>
<span data-ttu-id="350b1-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="350b1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="350b1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="350b1-119">-Name</span></span>
<span data-ttu-id="350b1-120">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="350b1-120">WebApp Name</span></span>

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

### <span data-ttu-id="350b1-121">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="350b1-121">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="350b1-122">Option "alle App-Einstellungsnamen entfernen"</span><span class="sxs-lookup"><span data-stu-id="350b1-122">Remove All App Setting Names Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="350b1-123">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="350b1-123">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="350b1-124">Option ' alle Namen für Verbindungszeichenfolgen entfernen '</span><span class="sxs-lookup"><span data-stu-id="350b1-124">Remove All Connection String Names Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="350b1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="350b1-125">-ResourceGroupName</span></span>
<span data-ttu-id="350b1-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="350b1-126">Resource Group Name</span></span>

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

### <span data-ttu-id="350b1-127">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="350b1-127">-WebApp</span></span>
<span data-ttu-id="350b1-128">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="350b1-128">WebApp Object</span></span>

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

### <span data-ttu-id="350b1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="350b1-129">CommonParameters</span></span>
<span data-ttu-id="350b1-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="350b1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="350b1-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="350b1-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="350b1-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="350b1-132">INPUTS</span></span>

### <span data-ttu-id="350b1-133">Website</span><span class="sxs-lookup"><span data-stu-id="350b1-133">Site</span></span>
<span data-ttu-id="350b1-134">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="350b1-134">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="350b1-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="350b1-135">OUTPUTS</span></span>

## <span data-ttu-id="350b1-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="350b1-136">NOTES</span></span>

## <span data-ttu-id="350b1-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="350b1-137">RELATED LINKS</span></span>


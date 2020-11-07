---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlotConfigName.md
ms.openlocfilehash: 5e2b13cd4c2586b15cc526aad3d922441b40265c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658498"
---
# <span data-ttu-id="2c413-101">Set-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="2c413-101">Set-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="2c413-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2c413-102">SYNOPSIS</span></span>
<span data-ttu-id="2c413-103">Einrichten von config-Namen für Web App-Steckplätze</span><span class="sxs-lookup"><span data-stu-id="2c413-103">Set Web App Slot Config names</span></span>

## <span data-ttu-id="2c413-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c413-104">SYNTAX</span></span>

### <span data-ttu-id="2c413-105">S1</span><span class="sxs-lookup"><span data-stu-id="2c413-105">S1</span></span>
```
Set-AzWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c413-106">S2</span><span class="sxs-lookup"><span data-stu-id="2c413-106">S2</span></span>
```
Set-AzWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c413-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2c413-107">DESCRIPTION</span></span>
<span data-ttu-id="2c413-108">Das Cmdlet " **Satz-AzWebAppSlotConfigName** " kennzeichnet App-Einstellungen und Verbindungszeichenfolgen als Steckplatz Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="2c413-108">The **Set-AzWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="2c413-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2c413-109">EXAMPLES</span></span>

### <span data-ttu-id="2c413-110">1:</span><span class="sxs-lookup"><span data-stu-id="2c413-110">1:</span></span>
```
PS C:\> Set-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="2c413-111">Dieser Befehl entfernt alle App-Einstellungen und Verbindungszeichenfolgen für Web-App-ContosoWebApp, die mit der Ressourcengruppe Standard verknüpft sind – Web-westus</span><span class="sxs-lookup"><span data-stu-id="2c413-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="2c413-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c413-112">PARAMETERS</span></span>

### <span data-ttu-id="2c413-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="2c413-113">-AppSettingNames</span></span>
<span data-ttu-id="2c413-114">Zeichenfolgen Array für App-Einstellungsnamen</span><span class="sxs-lookup"><span data-stu-id="2c413-114">App Settings Names String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c413-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="2c413-115">-ConnectionStringNames</span></span>
<span data-ttu-id="2c413-116">Zeichenfolgen Array für Verbindungszeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="2c413-116">Connection String Names String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c413-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c413-117">-DefaultProfile</span></span>
<span data-ttu-id="2c413-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2c413-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c413-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2c413-119">-Name</span></span>
<span data-ttu-id="2c413-120">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="2c413-120">WebApp Name</span></span>

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

### <span data-ttu-id="2c413-121">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="2c413-121">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="2c413-122">Option "alle App-Einstellungsnamen entfernen"</span><span class="sxs-lookup"><span data-stu-id="2c413-122">Remove All App Setting Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c413-123">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="2c413-123">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="2c413-124">Option ' alle Namen für Verbindungszeichenfolgen entfernen '</span><span class="sxs-lookup"><span data-stu-id="2c413-124">Remove All Connection String Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c413-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c413-125">-ResourceGroupName</span></span>
<span data-ttu-id="2c413-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="2c413-126">Resource Group Name</span></span>

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

### <span data-ttu-id="2c413-127">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="2c413-127">-WebApp</span></span>
<span data-ttu-id="2c413-128">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="2c413-128">WebApp Object</span></span>

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

### <span data-ttu-id="2c413-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c413-129">CommonParameters</span></span>
<span data-ttu-id="2c413-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c413-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c413-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c413-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c413-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2c413-132">INPUTS</span></span>

### <span data-ttu-id="2c413-133">System. String []</span><span class="sxs-lookup"><span data-stu-id="2c413-133">System.String[]</span></span>

### <span data-ttu-id="2c413-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2c413-134">System.String</span></span>

### <span data-ttu-id="2c413-135">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="2c413-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="2c413-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2c413-136">OUTPUTS</span></span>

### <span data-ttu-id="2c413-137">Microsoft. Azure. Management. Websites. Models. SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="2c413-137">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="2c413-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="2c413-138">NOTES</span></span>

## <span data-ttu-id="2c413-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2c413-139">RELATED LINKS</span></span>

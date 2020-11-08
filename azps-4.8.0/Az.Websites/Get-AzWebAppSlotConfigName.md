---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
ms.openlocfilehash: 9ca0578aacbd0ca970211bc38419880cbe99675b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165406"
---
# <span data-ttu-id="f69ba-101">Get-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="f69ba-101">Get-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="f69ba-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f69ba-102">SYNOPSIS</span></span>
<span data-ttu-id="f69ba-103">Abrufen der Liste der config-Namen für Web App-Steckplätze</span><span class="sxs-lookup"><span data-stu-id="f69ba-103">Get the list of Web App Slot Config names</span></span>

## <span data-ttu-id="f69ba-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f69ba-104">SYNTAX</span></span>

### <span data-ttu-id="f69ba-105">S1</span><span class="sxs-lookup"><span data-stu-id="f69ba-105">S1</span></span>
```
Get-AzWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f69ba-106">S2</span><span class="sxs-lookup"><span data-stu-id="f69ba-106">S2</span></span>
```
Get-AzWebAppSlotConfigName [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f69ba-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f69ba-107">DESCRIPTION</span></span>
<span data-ttu-id="f69ba-108">Das Cmdlet " **Get-AzWebAppSlotConfigName** " Ruft die Liste der App-Einstellungen und Verbindungszeichenfolgen-Namen ab, die derzeit als sloteinstellungen markiert sind.</span><span class="sxs-lookup"><span data-stu-id="f69ba-108">The **Get-AzWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="f69ba-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f69ba-109">EXAMPLES</span></span>

### <span data-ttu-id="f69ba-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f69ba-110">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="f69ba-111">Dieser Befehl ruft App-Einstellungen und Verbindungszeichenfolgen in Bezug auf die Web-App mit dem Namen ContosoSite ab, die der Ressourcengruppe Default-Web-westus zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f69ba-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="f69ba-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f69ba-112">PARAMETERS</span></span>

### <span data-ttu-id="f69ba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f69ba-113">-DefaultProfile</span></span>
<span data-ttu-id="f69ba-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f69ba-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f69ba-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f69ba-115">-Name</span></span>
<span data-ttu-id="f69ba-116">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="f69ba-116">WebApp Name</span></span>

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

### <span data-ttu-id="f69ba-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f69ba-117">-ResourceGroupName</span></span>
<span data-ttu-id="f69ba-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="f69ba-118">Resource Group Name</span></span>

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

### <span data-ttu-id="f69ba-119">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="f69ba-119">-WebApp</span></span>
<span data-ttu-id="f69ba-120">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="f69ba-120">WebApp Object</span></span>

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

### <span data-ttu-id="f69ba-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f69ba-121">CommonParameters</span></span>
<span data-ttu-id="f69ba-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f69ba-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f69ba-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f69ba-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f69ba-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f69ba-124">INPUTS</span></span>

### <span data-ttu-id="f69ba-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f69ba-125">System.String</span></span>

### <span data-ttu-id="f69ba-126">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="f69ba-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f69ba-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f69ba-127">OUTPUTS</span></span>

### <span data-ttu-id="f69ba-128">Microsoft. Azure. Management. Websites. Models. SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="f69ba-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="f69ba-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="f69ba-129">NOTES</span></span>

## <span data-ttu-id="f69ba-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f69ba-130">RELATED LINKS</span></span>

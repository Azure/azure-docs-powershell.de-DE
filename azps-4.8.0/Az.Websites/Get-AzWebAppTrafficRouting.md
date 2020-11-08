---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
ms.openlocfilehash: fb8d23ad24f8e9ab0b6e951d39ba7445d336176f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173638"
---
# <span data-ttu-id="364af-101">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="364af-101">Get-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="364af-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="364af-102">SYNOPSIS</span></span>
<span data-ttu-id="364af-103">Besorgen Sie sich eine Routingregel für den angegebenen Steckplatznamen.</span><span class="sxs-lookup"><span data-stu-id="364af-103">Get a routing Rule for the given Slot name.</span></span>

## <span data-ttu-id="364af-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="364af-104">SYNTAX</span></span>

```
Get-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="364af-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="364af-105">DESCRIPTION</span></span>
<span data-ttu-id="364af-106">Das Cmdlet " **Get-AzWebAppTrafficRouting** " Ruft eine Routingregelkonfiguration aus einem Azure Web App-Slot ab.</span><span class="sxs-lookup"><span data-stu-id="364af-106">The **Get-AzWebAppTrafficRouting** cmdlet Gets a routing rule configuration from an Azure Web App Slot.</span></span>

## <span data-ttu-id="364af-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="364af-107">EXAMPLES</span></span>

### <span data-ttu-id="364af-108">Beispiel 1 ruft die spezifische Routingregel aus dem Webablage-Steckplatz ab</span><span class="sxs-lookup"><span data-stu-id="364af-108">Example 1 Gets the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Get-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="364af-109">Mit diesem Befehl wird eine Routingregel für einen bestimmten webaktions Steckplatz abgerufen.</span><span class="sxs-lookup"><span data-stu-id="364af-109">This command gets a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="364af-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="364af-110">PARAMETERS</span></span>

### <span data-ttu-id="364af-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="364af-111">-DefaultProfile</span></span>
<span data-ttu-id="364af-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="364af-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="364af-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="364af-113">-ResourceGroupName</span></span>
<span data-ttu-id="364af-114">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="364af-114">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="364af-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="364af-115">-RuleName</span></span>
<span data-ttu-id="364af-116">Regelname</span><span class="sxs-lookup"><span data-stu-id="364af-116">Rule Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="364af-117">-Webbasierter</span><span class="sxs-lookup"><span data-stu-id="364af-117">-WebAppName</span></span>
<span data-ttu-id="364af-118">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="364af-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="364af-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="364af-119">CommonParameters</span></span>
<span data-ttu-id="364af-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="364af-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="364af-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="364af-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="364af-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="364af-122">INPUTS</span></span>

### <span data-ttu-id="364af-123">Keine</span><span class="sxs-lookup"><span data-stu-id="364af-123">None</span></span>

## <span data-ttu-id="364af-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="364af-124">OUTPUTS</span></span>

### <span data-ttu-id="364af-125">Microsoft. Azure. Management. Websites. Models. RampUpRule</span><span class="sxs-lookup"><span data-stu-id="364af-125">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="364af-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="364af-126">NOTES</span></span>

## <span data-ttu-id="364af-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="364af-127">RELATED LINKS</span></span>

[<span data-ttu-id="364af-128">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="364af-128">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="364af-129">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="364af-129">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="364af-130">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="364af-130">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)

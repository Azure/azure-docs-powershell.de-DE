---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azoffice365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
ms.openlocfilehash: 9e48bfd243133052f526f2b9adcbef2072cdd2cb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921792"
---
# <span data-ttu-id="29b55-101">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="29b55-101">New-AzOffice365PolicyProperty</span></span>

## <span data-ttu-id="29b55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29b55-102">SYNOPSIS</span></span>
<span data-ttu-id="29b55-103">Definieren Sie eine neue Office 365-Datenverkehrsbruchrichtlinie, die für eine Virtual Appliance-Website verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="29b55-103">Define a new Office 365 traffic breakout policy to be used with a Virtual Appliance site.</span></span>

## <span data-ttu-id="29b55-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29b55-104">SYNTAX</span></span>

```
New-AzOffice365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="29b55-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29b55-105">DESCRIPTION</span></span>
<span data-ttu-id="29b55-106">Der befehl New-AzOffice365PolicyProperties definiert eine Office 365-Breakoutrichtlinie, die mit einer Virtual Appliance-Website verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="29b55-106">The New-AzOffice365PolicyProperties command defines an Office 365 breakout policy that is to be used with a Virtual Appliance site.</span></span> 

## <span data-ttu-id="29b55-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="29b55-107">EXAMPLES</span></span>

### <span data-ttu-id="29b55-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="29b55-108">Example 1</span></span>
```powershell
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize 
```

<span data-ttu-id="29b55-109">Erstellen Sie ein Office 365-Richtlinienobjekt für Datenverkehrsbruch, das mit Den Virtual Appliance-Websitebefehlen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="29b55-109">Create Office 365 traffic breakout policy object to be used with Virtual Appliance site commands.</span></span>

## <span data-ttu-id="29b55-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="29b55-110">PARAMETERS</span></span>

### <span data-ttu-id="29b55-111">-Zulassen</span><span class="sxs-lookup"><span data-stu-id="29b55-111">-Allow</span></span>
<span data-ttu-id="29b55-112">Durchbrechen des Zulässigen Kategoriedatenverkehrs.</span><span class="sxs-lookup"><span data-stu-id="29b55-112">Breakout the allow category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29b55-113">-Standard</span><span class="sxs-lookup"><span data-stu-id="29b55-113">-Default</span></span>
<span data-ttu-id="29b55-114">Brechen Sie den standardmäßigen Kategoriedatenverkehr auf.</span><span class="sxs-lookup"><span data-stu-id="29b55-114">Breakout the default category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29b55-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29b55-115">-DefaultProfile</span></span>
<span data-ttu-id="29b55-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="29b55-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29b55-117">-Optimieren</span><span class="sxs-lookup"><span data-stu-id="29b55-117">-Optimize</span></span>
<span data-ttu-id="29b55-118">Brechen Sie den Datenverkehr der Kategorie optimieren ab.</span><span class="sxs-lookup"><span data-stu-id="29b55-118">Breakout the optimize category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29b55-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29b55-119">CommonParameters</span></span>
<span data-ttu-id="29b55-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29b55-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29b55-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29b55-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29b55-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="29b55-122">INPUTS</span></span>

### <span data-ttu-id="29b55-123">Keine</span><span class="sxs-lookup"><span data-stu-id="29b55-123">None</span></span>

## <span data-ttu-id="29b55-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="29b55-124">OUTPUTS</span></span>

### <span data-ttu-id="29b55-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="29b55-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

## <span data-ttu-id="29b55-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="29b55-126">NOTES</span></span>

## <span data-ttu-id="29b55-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="29b55-127">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeerasncontactdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
ms.openlocfilehash: 978c513646c08577f4fa15b8a0e460320878c7c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937704"
---
# <span data-ttu-id="0b25a-101">New-AzPeerAsnContactDetail</span><span class="sxs-lookup"><span data-stu-id="0b25a-101">New-AzPeerAsnContactDetail</span></span>

## <span data-ttu-id="0b25a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b25a-102">SYNOPSIS</span></span>
<span data-ttu-id="0b25a-103">Erstellt ein In-Memory-Kontakt-Detail für PeerAsn.</span><span class="sxs-lookup"><span data-stu-id="0b25a-103">Creates an in memory contact detail for PeerAsn.</span></span> 

## <span data-ttu-id="0b25a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b25a-104">SYNTAX</span></span>

```
New-AzPeerAsnContactDetail -Role <String> -Email <String> [-Phone <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b25a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b25a-105">DESCRIPTION</span></span>
<span data-ttu-id="0b25a-106">Erstellen Sie ein PeerAsn-Kontaktdetails im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="0b25a-106">Create an in memory PeerAsn contact detail.</span></span>

## <span data-ttu-id="0b25a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0b25a-107">EXAMPLES</span></span>

### <span data-ttu-id="0b25a-108">Erstellen von Kontaktdetails und Hinzufügen zu PeerAsn</span><span class="sxs-lookup"><span data-stu-id="0b25a-108">Create contact detail and add to PeerAsn</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact
```

<span data-ttu-id="0b25a-109">Rolle und E-Mail sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0b25a-109">Role and email are required.</span></span> <span data-ttu-id="0b25a-110">Telefon ist optional.</span><span class="sxs-lookup"><span data-stu-id="0b25a-110">Phone is optional.</span></span> <span data-ttu-id="0b25a-111">Telefon unterstützt +-() oder Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="0b25a-111">Phone supports +-() or spaces.</span></span> <span data-ttu-id="0b25a-112">Ein PeerAsn muss mindestens ein Kontaktdetail vom Typ "Noc" enthalten.</span><span class="sxs-lookup"><span data-stu-id="0b25a-112">A PeerAsn must include at least one contact detail of type "Noc"</span></span>

## <span data-ttu-id="0b25a-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0b25a-113">PARAMETERS</span></span>

### <span data-ttu-id="0b25a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b25a-114">-DefaultProfile</span></span>
<span data-ttu-id="0b25a-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0b25a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b25a-116">-E-Mail</span><span class="sxs-lookup"><span data-stu-id="0b25a-116">-Email</span></span>
<span data-ttu-id="0b25a-117">E-Mail-Adressen, die zum Kontakt verwendet werden, wenn probleme in der Regel ein Netzwerkbetriebscenter auftreten</span><span class="sxs-lookup"><span data-stu-id="0b25a-117">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="0b25a-118">-Phone</span><span class="sxs-lookup"><span data-stu-id="0b25a-118">-Phone</span></span>
<span data-ttu-id="0b25a-119">Telefon, das verwendet wird, um kontaktiert zu werden, wenn probleme in der Regel ein Netzwerkbetriebscenter auftreten</span><span class="sxs-lookup"><span data-stu-id="0b25a-119">Phone used to contact if issues arrise typically a Network Operations Center</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b25a-120">-Rolle</span><span class="sxs-lookup"><span data-stu-id="0b25a-120">-Role</span></span>
<span data-ttu-id="0b25a-121">Wählen Sie die Rolle aus, die den Kontaktinformationen am besten entspricht.</span><span class="sxs-lookup"><span data-stu-id="0b25a-121">Choose the role that best suits the contact information.</span></span>
<span data-ttu-id="0b25a-122">NOC-Kontakt ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0b25a-122">NOC Contact is required.</span></span>

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

### <span data-ttu-id="0b25a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b25a-123">CommonParameters</span></span>
<span data-ttu-id="0b25a-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b25a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b25a-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b25a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b25a-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0b25a-126">INPUTS</span></span>

### <span data-ttu-id="0b25a-127">Keine</span><span class="sxs-lookup"><span data-stu-id="0b25a-127">None</span></span>

## <span data-ttu-id="0b25a-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0b25a-128">OUTPUTS</span></span>

### <span data-ttu-id="0b25a-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span><span class="sxs-lookup"><span data-stu-id="0b25a-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span></span>

## <span data-ttu-id="0b25a-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0b25a-130">NOTES</span></span>

## <span data-ttu-id="0b25a-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0b25a-131">RELATED LINKS</span></span>

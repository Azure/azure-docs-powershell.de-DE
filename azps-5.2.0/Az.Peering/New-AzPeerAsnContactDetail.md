---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasncontactdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
ms.openlocfilehash: f2bba3b69205585cd6d8f4834803a82bf15ec305
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295793"
---
# <span data-ttu-id="106fb-101">New-AzPeerAsnContactDetail</span><span class="sxs-lookup"><span data-stu-id="106fb-101">New-AzPeerAsnContactDetail</span></span>

## <span data-ttu-id="106fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="106fb-102">SYNOPSIS</span></span>
<span data-ttu-id="106fb-103">Erstellt ein Detail im Speicherkontakt für PeerAsn.</span><span class="sxs-lookup"><span data-stu-id="106fb-103">Creates an in memory contact detail for PeerAsn.</span></span> 

## <span data-ttu-id="106fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="106fb-104">SYNTAX</span></span>

```
New-AzPeerAsnContactDetail -Role <String> -Email <String> [-Phone <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="106fb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="106fb-105">DESCRIPTION</span></span>
<span data-ttu-id="106fb-106">Erstellen Sie eine PeerAsn-Kontaktdetails im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="106fb-106">Create an in memory PeerAsn contact detail.</span></span>

## <span data-ttu-id="106fb-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="106fb-107">EXAMPLES</span></span>

### <span data-ttu-id="106fb-108">Erstellen von Kontaktdetails und Hinzufügen zu PeerAsn</span><span class="sxs-lookup"><span data-stu-id="106fb-108">Create contact detail and add to PeerAsn</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact
```

<span data-ttu-id="106fb-109">Rollen und E-Mail sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="106fb-109">Role and email are required.</span></span> <span data-ttu-id="106fb-110">Telefon ist optional.</span><span class="sxs-lookup"><span data-stu-id="106fb-110">Phone is optional.</span></span> <span data-ttu-id="106fb-111">Das Telefon unterstützt +-() oder Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="106fb-111">Phone supports +-() or spaces.</span></span> <span data-ttu-id="106fb-112">Ein PeerAsn muss mindestens ein Kontaktdetail vom Typ "Noc" enthalten.</span><span class="sxs-lookup"><span data-stu-id="106fb-112">A PeerAsn must include at least one contact detail of type "Noc"</span></span>

## <span data-ttu-id="106fb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="106fb-113">PARAMETERS</span></span>

### <span data-ttu-id="106fb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="106fb-114">-DefaultProfile</span></span>
<span data-ttu-id="106fb-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="106fb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="106fb-116">-Email</span><span class="sxs-lookup"><span data-stu-id="106fb-116">-Email</span></span>
<span data-ttu-id="106fb-117">E-Mail-Adressen, die zum Kontakt verwendet werden, wenn probleme in der Regel ein Netzwerkbetriebscenter auftreten</span><span class="sxs-lookup"><span data-stu-id="106fb-117">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="106fb-118">-Phone</span><span class="sxs-lookup"><span data-stu-id="106fb-118">-Phone</span></span>
<span data-ttu-id="106fb-119">Telefon, mit dem kontaktiert wird, wenn probleme in der Regel ein Netzwerkbetriebscenter auftreten</span><span class="sxs-lookup"><span data-stu-id="106fb-119">Phone used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="106fb-120">-Role</span><span class="sxs-lookup"><span data-stu-id="106fb-120">-Role</span></span>
<span data-ttu-id="106fb-121">Wählen Sie die Rolle aus, die den Kontaktinformationen am besten entspricht.</span><span class="sxs-lookup"><span data-stu-id="106fb-121">Choose the role that best suits the contact information.</span></span>
<span data-ttu-id="106fb-122">"NOC-Kontakt" ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="106fb-122">NOC Contact is required.</span></span>

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

### <span data-ttu-id="106fb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="106fb-123">CommonParameters</span></span>
<span data-ttu-id="106fb-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="106fb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="106fb-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="106fb-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="106fb-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="106fb-126">INPUTS</span></span>

### <span data-ttu-id="106fb-127">Keine</span><span class="sxs-lookup"><span data-stu-id="106fb-127">None</span></span>

## <span data-ttu-id="106fb-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="106fb-128">OUTPUTS</span></span>

### <span data-ttu-id="106fb-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span><span class="sxs-lookup"><span data-stu-id="106fb-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span></span>

## <span data-ttu-id="106fb-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="106fb-130">NOTES</span></span>

## <span data-ttu-id="106fb-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="106fb-131">RELATED LINKS</span></span>

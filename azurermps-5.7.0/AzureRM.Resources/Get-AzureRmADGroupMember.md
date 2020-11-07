---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
ms.openlocfilehash: c3a783178bf8342e891f8eab2996e77a2045721a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663760"
---
# <span data-ttu-id="fb2df-101">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="fb2df-101">Get-AzureRmADGroupMember</span></span>

## <span data-ttu-id="fb2df-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fb2df-102">SYNOPSIS</span></span>
<span data-ttu-id="fb2df-103">Besorgen Sie sich eine Gruppenmitglieder.</span><span class="sxs-lookup"><span data-stu-id="fb2df-103">Get a group members.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb2df-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb2df-104">SYNTAX</span></span>

```
Get-AzureRmADGroupMember [-GroupObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb2df-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb2df-105">DESCRIPTION</span></span>
<span data-ttu-id="fb2df-106">Besorgen Sie sich eine Gruppenmitglieder.</span><span class="sxs-lookup"><span data-stu-id="fb2df-106">Get a group members.</span></span>

## <span data-ttu-id="fb2df-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fb2df-107">EXAMPLES</span></span>

### <span data-ttu-id="fb2df-108">Filtert Gruppenmitglieder mit der Gruppenobjekt-ID</span><span class="sxs-lookup"><span data-stu-id="fb2df-108">Filters group members using group object id</span></span>
```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="fb2df-109">Ruft Gruppenmitglieder mit 85F89C90-780E-4AA6-9F4F-6F268D322EEE-ID ab</span><span class="sxs-lookup"><span data-stu-id="fb2df-109">Gets group members with 85F89C90-780E-4AA6-9F4F-6F268D322EEE id</span></span>

## <span data-ttu-id="fb2df-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb2df-110">PARAMETERS</span></span>

### <span data-ttu-id="fb2df-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb2df-111">-DefaultProfile</span></span>
<span data-ttu-id="fb2df-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="fb2df-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb2df-113">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="fb2df-113">-GroupObjectId</span></span>
<span data-ttu-id="fb2df-114">Objekt-ID der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="fb2df-114">Object id of the group.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb2df-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb2df-115">CommonParameters</span></span>
<span data-ttu-id="fb2df-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb2df-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb2df-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb2df-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb2df-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fb2df-118">INPUTS</span></span>

### <span data-ttu-id="fb2df-119">Keine</span><span class="sxs-lookup"><span data-stu-id="fb2df-119">None</span></span>
<span data-ttu-id="fb2df-120">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="fb2df-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fb2df-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fb2df-121">OUTPUTS</span></span>

### <span data-ttu-id="fb2df-122">System. Collections. Generic. List ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADObject]</span><span class="sxs-lookup"><span data-stu-id="fb2df-122">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADObject]</span></span>

## <span data-ttu-id="fb2df-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="fb2df-123">NOTES</span></span>

## <span data-ttu-id="fb2df-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fb2df-124">RELATED LINKS</span></span>

[<span data-ttu-id="fb2df-125">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="fb2df-125">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="fb2df-126">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="fb2df-126">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)


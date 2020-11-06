---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
ms.openlocfilehash: 1079486422da769863e86d3fc16d1c3ec65d6f5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481621"
---
# <span data-ttu-id="c3333-101">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="c3333-101">Get-AzureRmADGroup</span></span>

## <span data-ttu-id="c3333-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c3333-102">SYNOPSIS</span></span>
<span data-ttu-id="c3333-103">Filtert Active Directory-Gruppen.</span><span class="sxs-lookup"><span data-stu-id="c3333-103">Filters active directory groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3333-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3333-104">SYNTAX</span></span>

### <span data-ttu-id="c3333-105">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c3333-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3333-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3333-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADGroup -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3333-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3333-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3333-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3333-108">DESCRIPTION</span></span>
<span data-ttu-id="c3333-109">Filtert Active Directory-Gruppen.</span><span class="sxs-lookup"><span data-stu-id="c3333-109">Filters active directory groups.</span></span>

## <span data-ttu-id="c3333-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c3333-110">EXAMPLES</span></span>

### <span data-ttu-id="c3333-111">--------------------------Filtert Gruppen mithilfe der Objekt-ID--------------------------</span><span class="sxs-lookup"><span data-stu-id="c3333-111">--------------------------  Filters groups using object id  --------------------------</span></span>
```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="c3333-112">Ruft die Gruppe mit der 85F89C90-780E-4AA6-9F4F-6F268D322EEE-ID ab</span><span class="sxs-lookup"><span data-stu-id="c3333-112">Gets group with 85F89C90-780E-4AA6-9F4F-6F268D322EEE id</span></span>

### <span data-ttu-id="c3333-113">--------------------------Filtert Gruppen mithilfe der Suchzeichenfolge--------------------------</span><span class="sxs-lookup"><span data-stu-id="c3333-113">--------------------------  Filters groups using Search String  --------------------------</span></span>
```
PS C:\> Get-AzureRmADGroup -SearchString Joe
```

<span data-ttu-id="c3333-114">Filtert alle Anzeigengruppen, die Joe im Anzeigenamen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c3333-114">Filters all ad groups that has Joe in the display name.</span></span>

### <span data-ttu-id="c3333-115">--------------------------Listen Anzeigengruppen--------------------------</span><span class="sxs-lookup"><span data-stu-id="c3333-115">--------------------------  List AD groups  --------------------------</span></span>
```
PS C:\> Get-AzureRmADGroup
```

<span data-ttu-id="c3333-116">Ruft alle Anzeigengruppen ab</span><span class="sxs-lookup"><span data-stu-id="c3333-116">Gets all AD groups</span></span>

## <span data-ttu-id="c3333-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3333-117">PARAMETERS</span></span>

### <span data-ttu-id="c3333-118">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="c3333-118">-ObjectId</span></span>
<span data-ttu-id="c3333-119">Objekt-ID der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="c3333-119">Object id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3333-120">-Search-Funktion</span><span class="sxs-lookup"><span data-stu-id="c3333-120">-SearchString</span></span>
<span data-ttu-id="c3333-121">Der Anzeigename der Gruppe</span><span class="sxs-lookup"><span data-stu-id="c3333-121">The group display name</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3333-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3333-122">-DefaultProfile</span></span>
<span data-ttu-id="c3333-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c3333-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3333-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3333-124">CommonParameters</span></span>
<span data-ttu-id="c3333-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3333-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3333-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3333-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3333-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c3333-127">INPUTS</span></span>

## <span data-ttu-id="c3333-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c3333-128">OUTPUTS</span></span>

### <span data-ttu-id="c3333-129">System. Collections. Generic. List ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup]</span><span class="sxs-lookup"><span data-stu-id="c3333-129">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup]</span></span>

## <span data-ttu-id="c3333-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="c3333-130">NOTES</span></span>

## <span data-ttu-id="c3333-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c3333-131">RELATED LINKS</span></span>

[<span data-ttu-id="c3333-132">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="c3333-132">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="c3333-133">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c3333-133">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="c3333-134">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="c3333-134">Get-AzureRmADGroupMember</span></span>](./Get-AzureRmADGroupMember.md)


---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
ms.openlocfilehash: 29c3a76817bd50a5f86ea051b6de1139980a0dba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501426"
---
# <span data-ttu-id="931c2-101">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="931c2-101">Get-AzureRmADGroup</span></span>

## <span data-ttu-id="931c2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="931c2-102">SYNOPSIS</span></span>
<span data-ttu-id="931c2-103">Filtert Active Directory-Gruppen.</span><span class="sxs-lookup"><span data-stu-id="931c2-103">Filters active directory groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="931c2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="931c2-104">SYNTAX</span></span>

### <span data-ttu-id="931c2-105">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="931c2-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="931c2-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="931c2-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADGroup -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="931c2-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="931c2-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="931c2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="931c2-108">DESCRIPTION</span></span>
<span data-ttu-id="931c2-109">Filtert Active Directory-Gruppen.</span><span class="sxs-lookup"><span data-stu-id="931c2-109">Filters active directory groups.</span></span>

## <span data-ttu-id="931c2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="931c2-110">EXAMPLES</span></span>

### <span data-ttu-id="931c2-111">Filtert Gruppen mit der Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="931c2-111">Filters groups using object id</span></span>
```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="931c2-112">Ruft die Gruppe mit der 85F89C90-780E-4AA6-9F4F-6F268D322EEE-ID ab</span><span class="sxs-lookup"><span data-stu-id="931c2-112">Gets group with 85F89C90-780E-4AA6-9F4F-6F268D322EEE id</span></span>

### <span data-ttu-id="931c2-113">Filtert Gruppen mithilfe der Suchzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="931c2-113">Filters groups using Search String</span></span>
```
PS C:\> Get-AzureRmADGroup -SearchString Joe
```

<span data-ttu-id="931c2-114">Filtert alle Anzeigengruppen, die Joe im Anzeigenamen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="931c2-114">Filters all ad groups that has Joe in the display name.</span></span>

### <span data-ttu-id="931c2-115">Anzeigengruppen auflisten</span><span class="sxs-lookup"><span data-stu-id="931c2-115">List AD groups</span></span>
```
PS C:\> Get-AzureRmADGroup
```

<span data-ttu-id="931c2-116">Ruft alle Anzeigengruppen ab</span><span class="sxs-lookup"><span data-stu-id="931c2-116">Gets all AD groups</span></span>

## <span data-ttu-id="931c2-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="931c2-117">PARAMETERS</span></span>

### <span data-ttu-id="931c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="931c2-118">-DefaultProfile</span></span>
<span data-ttu-id="931c2-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="931c2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="931c2-120">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="931c2-120">-ObjectId</span></span>
<span data-ttu-id="931c2-121">Objekt-ID der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="931c2-121">Object id of the group.</span></span>

```yaml
Type: Guid
Parameter Sets: EmptyParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="931c2-122">-Search-Funktion</span><span class="sxs-lookup"><span data-stu-id="931c2-122">-SearchString</span></span>
<span data-ttu-id="931c2-123">Der Anzeigename der Gruppe</span><span class="sxs-lookup"><span data-stu-id="931c2-123">The group display name</span></span>

```yaml
Type: String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="931c2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="931c2-124">CommonParameters</span></span>
<span data-ttu-id="931c2-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="931c2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="931c2-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="931c2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="931c2-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="931c2-127">INPUTS</span></span>

### <span data-ttu-id="931c2-128">Keine</span><span class="sxs-lookup"><span data-stu-id="931c2-128">None</span></span>
<span data-ttu-id="931c2-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="931c2-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="931c2-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="931c2-130">OUTPUTS</span></span>

### <span data-ttu-id="931c2-131">System. Collections. Generic. List ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup]</span><span class="sxs-lookup"><span data-stu-id="931c2-131">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup]</span></span>

## <span data-ttu-id="931c2-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="931c2-132">NOTES</span></span>

## <span data-ttu-id="931c2-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="931c2-133">RELATED LINKS</span></span>

[<span data-ttu-id="931c2-134">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="931c2-134">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="931c2-135">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="931c2-135">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="931c2-136">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="931c2-136">Get-AzureRmADGroupMember</span></span>](./Get-AzureRmADGroupMember.md)


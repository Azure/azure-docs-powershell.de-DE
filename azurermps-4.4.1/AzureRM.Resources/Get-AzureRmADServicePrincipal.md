---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
ms.openlocfilehash: 34f4b85a299e714f524b1a4d33f2fb717483c377
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503962"
---
# <span data-ttu-id="61d8c-101">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="61d8c-101">Get-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="61d8c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="61d8c-102">SYNOPSIS</span></span>
<span data-ttu-id="61d8c-103">Filtert Active Directory-Dienst Prinzipale.</span><span class="sxs-lookup"><span data-stu-id="61d8c-103">Filters active directory service principals.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61d8c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="61d8c-104">SYNTAX</span></span>

### <span data-ttu-id="61d8c-105">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="61d8c-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADServicePrincipal [-ServicePrincipalName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="61d8c-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="61d8c-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -SearchString <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="61d8c-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61d8c-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61d8c-108">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="61d8c-108">SPNParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="61d8c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61d8c-109">DESCRIPTION</span></span>
<span data-ttu-id="61d8c-110">Filtert Active Directory-Dienst Prinzipale.</span><span class="sxs-lookup"><span data-stu-id="61d8c-110">Filters active directory service principals.</span></span>

## <span data-ttu-id="61d8c-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="61d8c-111">EXAMPLES</span></span>

### <span data-ttu-id="61d8c-112">--------------------------Filtert Dienst Prinzipale mithilfe von SPN--------------------------</span><span class="sxs-lookup"><span data-stu-id="61d8c-112">--------------------------  Filters service principals using SPN  --------------------------</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal -SPN 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="61d8c-113">Ruft Dienst Prinzipale mit dem 36f81fc3-b00f-48cd-8218-3879f51ff39f-SPN ab.</span><span class="sxs-lookup"><span data-stu-id="61d8c-113">Gets service principals with 36f81fc3-b00f-48cd-8218-3879f51ff39f SPN.</span></span>

### <span data-ttu-id="61d8c-114">--------------------------Filtert Dienst Prinzipale mithilfe der Suchzeichenfolge--------------------------</span><span class="sxs-lookup"><span data-stu-id="61d8c-114">--------------------------  Filters service principals using Search String  --------------------------</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="61d8c-115">Filtert alle Anzeigendienst Prinzipale, die den Anzeigenamen aufweisen, beginnend mit "Web".</span><span class="sxs-lookup"><span data-stu-id="61d8c-115">Filters all ad service principals that have display name starting with "Web".</span></span>

### <span data-ttu-id="61d8c-116">--------------------------Liste Anzeigendienst Prinzipale--------------------------</span><span class="sxs-lookup"><span data-stu-id="61d8c-116">--------------------------  List AD service principals  --------------------------</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal
```

<span data-ttu-id="61d8c-117">Ruft alle Anzeigendienst Prinzipale ab.</span><span class="sxs-lookup"><span data-stu-id="61d8c-117">Gets all AD service principals.</span></span>

## <span data-ttu-id="61d8c-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="61d8c-118">PARAMETERS</span></span>

### <span data-ttu-id="61d8c-119">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="61d8c-119">-ObjectId</span></span>
<span data-ttu-id="61d8c-120">Objekt-ID des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="61d8c-120">Object id of the service principal.</span></span>

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

### <span data-ttu-id="61d8c-121">-Search-Funktion</span><span class="sxs-lookup"><span data-stu-id="61d8c-121">-SearchString</span></span>
<span data-ttu-id="61d8c-122">Ruft alle Dienst Prinzipale ab, deren Anzeigenamen mit diesem Wert beginnen.</span><span class="sxs-lookup"><span data-stu-id="61d8c-122">Fetches all service principals that have the display name starting with this value.</span></span>

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

### <span data-ttu-id="61d8c-123">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="61d8c-123">-ServicePrincipalName</span></span>
<span data-ttu-id="61d8c-124">SPN des Diensts.</span><span class="sxs-lookup"><span data-stu-id="61d8c-124">SPN of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet
Aliases: SPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61d8c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61d8c-125">-DefaultProfile</span></span>
<span data-ttu-id="61d8c-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="61d8c-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61d8c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61d8c-127">CommonParameters</span></span>
<span data-ttu-id="61d8c-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61d8c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61d8c-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61d8c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61d8c-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="61d8c-130">INPUTS</span></span>

## <span data-ttu-id="61d8c-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="61d8c-131">OUTPUTS</span></span>

### <span data-ttu-id="61d8c-132">System. Collections. Generic. List ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal]</span><span class="sxs-lookup"><span data-stu-id="61d8c-132">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal]</span></span>

## <span data-ttu-id="61d8c-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="61d8c-133">NOTES</span></span>

## <span data-ttu-id="61d8c-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="61d8c-134">RELATED LINKS</span></span>

[<span data-ttu-id="61d8c-135">Neu – AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="61d8c-135">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="61d8c-136">Satz-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="61d8c-136">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="61d8c-137">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="61d8c-137">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="61d8c-138">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="61d8c-138">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="61d8c-139">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="61d8c-139">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)


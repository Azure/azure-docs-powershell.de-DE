---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
ms.openlocfilehash: 8344d9e794189d67a69c1be9a88e135b721a0d4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480973"
---
# <span data-ttu-id="29080-101">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="29080-101">Get-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="29080-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="29080-102">SYNOPSIS</span></span>
<span data-ttu-id="29080-103">Filtert Active Directory-Dienst Prinzipale.</span><span class="sxs-lookup"><span data-stu-id="29080-103">Filters active directory service principals.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29080-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="29080-104">SYNTAX</span></span>

### <span data-ttu-id="29080-105">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="29080-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29080-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="29080-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -SearchString <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="29080-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="29080-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29080-108">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="29080-108">SPNParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="29080-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29080-109">DESCRIPTION</span></span>
<span data-ttu-id="29080-110">Filtert Active Directory-Dienst Prinzipale.</span><span class="sxs-lookup"><span data-stu-id="29080-110">Filters active directory service principals.</span></span>

## <span data-ttu-id="29080-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="29080-111">EXAMPLES</span></span>

### <span data-ttu-id="29080-112">Filtert Dienst Prinzipale mithilfe von SPN</span><span class="sxs-lookup"><span data-stu-id="29080-112">Filters service principals using SPN</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal -SPN 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="29080-113">Ruft Dienst Prinzipale mit dem 36f81fc3-b00f-48cd-8218-3879f51ff39f-SPN ab.</span><span class="sxs-lookup"><span data-stu-id="29080-113">Gets service principals with 36f81fc3-b00f-48cd-8218-3879f51ff39f SPN.</span></span>

### <span data-ttu-id="29080-114">Filtert Dienst Prinzipale mithilfe der Suchzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="29080-114">Filters service principals using Search String</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="29080-115">Filtert alle Anzeigendienst Prinzipale, die den Anzeigenamen aufweisen, beginnend mit "Web".</span><span class="sxs-lookup"><span data-stu-id="29080-115">Filters all ad service principals that have display name starting with "Web".</span></span>

### <span data-ttu-id="29080-116">Anzeigendienst Prinzipale auflisten</span><span class="sxs-lookup"><span data-stu-id="29080-116">List AD service principals</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal
```

<span data-ttu-id="29080-117">Ruft alle Anzeigendienst Prinzipale ab.</span><span class="sxs-lookup"><span data-stu-id="29080-117">Gets all AD service principals.</span></span>

## <span data-ttu-id="29080-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="29080-118">PARAMETERS</span></span>

### <span data-ttu-id="29080-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29080-119">-DefaultProfile</span></span>
<span data-ttu-id="29080-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="29080-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29080-121">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="29080-121">-ObjectId</span></span>
<span data-ttu-id="29080-122">Objekt-ID des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="29080-122">Object id of the service principal.</span></span>

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

### <span data-ttu-id="29080-123">-Search-Funktion</span><span class="sxs-lookup"><span data-stu-id="29080-123">-SearchString</span></span>
<span data-ttu-id="29080-124">Ruft alle Dienst Prinzipale ab, deren Anzeigenamen mit diesem Wert beginnen.</span><span class="sxs-lookup"><span data-stu-id="29080-124">Fetches all service principals that have the display name starting with this value.</span></span>

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

### <span data-ttu-id="29080-125">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="29080-125">-ServicePrincipalName</span></span>
<span data-ttu-id="29080-126">SPN des Diensts.</span><span class="sxs-lookup"><span data-stu-id="29080-126">SPN of the service.</span></span>

```yaml
Type: String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29080-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29080-127">CommonParameters</span></span>
<span data-ttu-id="29080-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29080-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29080-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29080-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29080-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="29080-130">INPUTS</span></span>

### <span data-ttu-id="29080-131">Keine</span><span class="sxs-lookup"><span data-stu-id="29080-131">None</span></span>
<span data-ttu-id="29080-132">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="29080-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="29080-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="29080-133">OUTPUTS</span></span>

### <span data-ttu-id="29080-134">System. Collections. Generic. List ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal]</span><span class="sxs-lookup"><span data-stu-id="29080-134">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal]</span></span>

## <span data-ttu-id="29080-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="29080-135">NOTES</span></span>

## <span data-ttu-id="29080-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="29080-136">RELATED LINKS</span></span>

[<span data-ttu-id="29080-137">Neu – AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="29080-137">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="29080-138">Satz-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="29080-138">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="29080-139">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="29080-139">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="29080-140">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="29080-140">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="29080-141">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="29080-141">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)


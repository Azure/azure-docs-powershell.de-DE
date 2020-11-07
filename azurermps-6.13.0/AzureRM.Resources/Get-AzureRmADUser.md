---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
ms.openlocfilehash: b19571025aeb6349277e9ae366146774862e8a80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662791"
---
# <span data-ttu-id="7a32a-101">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="7a32a-101">Get-AzureRmADUser</span></span>

## <span data-ttu-id="7a32a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7a32a-102">SYNOPSIS</span></span>
<span data-ttu-id="7a32a-103">Filtert Active Directory-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="7a32a-103">Filters active directory users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a32a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a32a-104">SYNTAX</span></span>

### <span data-ttu-id="7a32a-105">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7a32a-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7a32a-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a32a-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7a32a-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a32a-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7a32a-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a32a-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7a32a-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a32a-109">UPNParameterSet</span></span>
```
Get-AzureRmADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7a32a-110">Mailparameterset</span><span class="sxs-lookup"><span data-stu-id="7a32a-110">MailParameterSet</span></span>
```
Get-AzureRmADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="7a32a-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7a32a-111">DESCRIPTION</span></span>
<span data-ttu-id="7a32a-112">Filtert Active Directory-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="7a32a-112">Filters active directory users.</span></span>

## <span data-ttu-id="7a32a-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7a32a-113">EXAMPLES</span></span>

### <span data-ttu-id="7a32a-114">Beispiel 1 – Auflisten aller Benutzer</span><span class="sxs-lookup"><span data-stu-id="7a32a-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzureRmADUser
```

<span data-ttu-id="7a32a-115">Listet alle anzeigen Benutzer in einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="7a32a-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="7a32a-116">Beispiel 2 – Auflisten aller Benutzer, die Paging verwenden</span><span class="sxs-lookup"><span data-stu-id="7a32a-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzureRmADUser -First 100
```

<span data-ttu-id="7a32a-117">Listet die ersten 100-anzeigen Benutzer in einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="7a32a-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="7a32a-118">Beispiel 3: Abrufen des anzeigen Benutzers nach dem Benutzerprinzipalnamen</span><span class="sxs-lookup"><span data-stu-id="7a32a-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzureRmADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="7a32a-119">Ruft den anzeigen Benutzer mit dem Benutzerprinzipalnamen " foo@domain.com " ab.</span><span class="sxs-lookup"><span data-stu-id="7a32a-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="7a32a-120">Beispiel 4 – Liste nach Suchzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7a32a-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzureRmADUser -SearchString Joe
```

<span data-ttu-id="7a32a-121">Listet alle anzeigen Benutzer auf, deren Anzeigename mit "Joe" beginnt.</span><span class="sxs-lookup"><span data-stu-id="7a32a-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="7a32a-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a32a-122">PARAMETERS</span></span>

### <span data-ttu-id="7a32a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a32a-123">-DefaultProfile</span></span>
<span data-ttu-id="7a32a-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7a32a-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a32a-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7a32a-125">-DisplayName</span></span>
<span data-ttu-id="7a32a-126">Der Anzeigename des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="7a32a-126">The display name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a32a-127">-First</span><span class="sxs-lookup"><span data-stu-id="7a32a-127">-First</span></span>
<span data-ttu-id="7a32a-128">Die maximale Anzahl von Objekten, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7a32a-128">The maximum number of objects to return.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a32a-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="7a32a-129">-IncludeTotalCount</span></span>
<span data-ttu-id="7a32a-130">Gibt die Anzahl der Objekte in der Datengruppe an.</span><span class="sxs-lookup"><span data-stu-id="7a32a-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="7a32a-131">Derzeit hat dieser Parameter keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="7a32a-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="7a32a-132">-Mail</span><span class="sxs-lookup"><span data-stu-id="7a32a-132">-Mail</span></span>
<span data-ttu-id="7a32a-133">Die Benutzer-e-Mail.</span><span class="sxs-lookup"><span data-stu-id="7a32a-133">The user mail.</span></span>

```yaml
Type: System.String
Parameter Sets: MailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a32a-134">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="7a32a-134">-ObjectId</span></span>
<span data-ttu-id="7a32a-135">Objekt-ID des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="7a32a-135">Object id of the user.</span></span>

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

### <span data-ttu-id="7a32a-136">-Skip</span><span class="sxs-lookup"><span data-stu-id="7a32a-136">-Skip</span></span>
<span data-ttu-id="7a32a-137">Ignoriert die ersten N Objekte und ruft dann die restlichen Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="7a32a-137">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a32a-138">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="7a32a-138">-StartsWith</span></span>
<span data-ttu-id="7a32a-139">Wird verwendet, um Benutzer zu finden, die mit der bereitgestellten Zeichenfolge beginnen.</span><span class="sxs-lookup"><span data-stu-id="7a32a-139">Used to find users that begin with the provided string.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: SearchString

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a32a-140">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="7a32a-140">-UserPrincipalName</span></span>
<span data-ttu-id="7a32a-141">UPN des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="7a32a-141">UPN of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet
Aliases: UPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a32a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a32a-142">CommonParameters</span></span>
<span data-ttu-id="7a32a-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a32a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a32a-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a32a-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a32a-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7a32a-145">INPUTS</span></span>

### <span data-ttu-id="7a32a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="7a32a-146">System.String</span></span>

### <span data-ttu-id="7a32a-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="7a32a-147">System.Guid</span></span>

## <span data-ttu-id="7a32a-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7a32a-148">OUTPUTS</span></span>

### <span data-ttu-id="7a32a-149">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="7a32a-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="7a32a-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="7a32a-150">NOTES</span></span>

## <span data-ttu-id="7a32a-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7a32a-151">RELATED LINKS</span></span>

[<span data-ttu-id="7a32a-152">Neu – AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="7a32a-152">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="7a32a-153">Satz-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="7a32a-153">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="7a32a-154">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="7a32a-154">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)


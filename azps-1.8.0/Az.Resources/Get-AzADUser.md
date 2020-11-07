---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: 910df03db722636e91e95ff1c6aad7898b333740
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659654"
---
# <span data-ttu-id="9bd60-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="9bd60-101">Get-AzADUser</span></span>

## <span data-ttu-id="9bd60-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9bd60-102">SYNOPSIS</span></span>
<span data-ttu-id="9bd60-103">Filtert Active Directory-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="9bd60-103">Filters active directory users.</span></span>

## <span data-ttu-id="9bd60-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9bd60-104">SYNTAX</span></span>

### <span data-ttu-id="9bd60-105">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9bd60-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="9bd60-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bd60-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="9bd60-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bd60-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="9bd60-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bd60-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="9bd60-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bd60-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="9bd60-110">Mailparameterset</span><span class="sxs-lookup"><span data-stu-id="9bd60-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="9bd60-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9bd60-111">DESCRIPTION</span></span>
<span data-ttu-id="9bd60-112">Filtert Active Directory-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="9bd60-112">Filters active directory users.</span></span>

## <span data-ttu-id="9bd60-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9bd60-113">EXAMPLES</span></span>

### <span data-ttu-id="9bd60-114">Beispiel 1 – Auflisten aller Benutzer</span><span class="sxs-lookup"><span data-stu-id="9bd60-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzADUser
```

<span data-ttu-id="9bd60-115">Listet alle anzeigen Benutzer in einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="9bd60-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="9bd60-116">Beispiel 2 – Auflisten aller Benutzer, die Paging verwenden</span><span class="sxs-lookup"><span data-stu-id="9bd60-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="9bd60-117">Listet die ersten 100-anzeigen Benutzer in einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="9bd60-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="9bd60-118">Beispiel 3: Abrufen des anzeigen Benutzers nach dem Benutzerprinzipalnamen</span><span class="sxs-lookup"><span data-stu-id="9bd60-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="9bd60-119">Ruft den anzeigen Benutzer mit dem Benutzerprinzipalnamen " foo@domain.com " ab.</span><span class="sxs-lookup"><span data-stu-id="9bd60-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="9bd60-120">Beispiel 4 – Liste nach Suchzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9bd60-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="9bd60-121">Listet alle anzeigen Benutzer auf, deren Anzeigename mit "Joe" beginnt.</span><span class="sxs-lookup"><span data-stu-id="9bd60-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="9bd60-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="9bd60-122">PARAMETERS</span></span>

### <span data-ttu-id="9bd60-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bd60-123">-DefaultProfile</span></span>
<span data-ttu-id="9bd60-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9bd60-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9bd60-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9bd60-125">-DisplayName</span></span>
<span data-ttu-id="9bd60-126">Der Anzeigename des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="9bd60-126">The display name of the user.</span></span>

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

### <span data-ttu-id="9bd60-127">-Mail</span><span class="sxs-lookup"><span data-stu-id="9bd60-127">-Mail</span></span>
<span data-ttu-id="9bd60-128">Die Benutzer-e-Mail.</span><span class="sxs-lookup"><span data-stu-id="9bd60-128">The user mail.</span></span>

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

### <span data-ttu-id="9bd60-129">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="9bd60-129">-ObjectId</span></span>
<span data-ttu-id="9bd60-130">Objekt-ID des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="9bd60-130">Object id of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bd60-131">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="9bd60-131">-StartsWith</span></span>
<span data-ttu-id="9bd60-132">Wird verwendet, um Benutzer zu finden, die mit der bereitgestellten Zeichenfolge beginnen.</span><span class="sxs-lookup"><span data-stu-id="9bd60-132">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="9bd60-133">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="9bd60-133">-UserPrincipalName</span></span>
<span data-ttu-id="9bd60-134">UPN des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="9bd60-134">UPN of the user.</span></span>

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

### <span data-ttu-id="9bd60-135">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="9bd60-135">-IncludeTotalCount</span></span>
<span data-ttu-id="9bd60-136">Gibt die Anzahl der Objekte in der Datengruppe an.</span><span class="sxs-lookup"><span data-stu-id="9bd60-136">Reports the number of objects in the data set.</span></span> <span data-ttu-id="9bd60-137">Derzeit hat dieser Parameter keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="9bd60-137">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="9bd60-138">-Skip</span><span class="sxs-lookup"><span data-stu-id="9bd60-138">-Skip</span></span>
<span data-ttu-id="9bd60-139">Ignoriert die ersten N Objekte und ruft dann die restlichen Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="9bd60-139">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="9bd60-140">-First</span><span class="sxs-lookup"><span data-stu-id="9bd60-140">-First</span></span>
<span data-ttu-id="9bd60-141">Die maximale Anzahl von Objekten, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9bd60-141">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="9bd60-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bd60-142">CommonParameters</span></span>
<span data-ttu-id="9bd60-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bd60-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bd60-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bd60-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bd60-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9bd60-145">INPUTS</span></span>

### <span data-ttu-id="9bd60-146">System. String</span><span class="sxs-lookup"><span data-stu-id="9bd60-146">System.String</span></span>

## <span data-ttu-id="9bd60-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9bd60-147">OUTPUTS</span></span>

### <span data-ttu-id="9bd60-148">Microsoft. Azure. Commands. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="9bd60-148">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="9bd60-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="9bd60-149">NOTES</span></span>

## <span data-ttu-id="9bd60-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9bd60-150">RELATED LINKS</span></span>

[<span data-ttu-id="9bd60-151">Neu – AzADUser</span><span class="sxs-lookup"><span data-stu-id="9bd60-151">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="9bd60-152">Satz-AzADUser</span><span class="sxs-lookup"><span data-stu-id="9bd60-152">Set-AzADUser</span></span>](./Set-AzADUser.md)

[<span data-ttu-id="9bd60-153">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="9bd60-153">Remove-AzADUser</span></span>](./Remove-AzADUser.md)


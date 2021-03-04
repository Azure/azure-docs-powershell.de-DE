---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
ms.openlocfilehash: 83212224ba14e0a079db936d058522d4759430fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923464"
---
# <span data-ttu-id="59d72-101">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="59d72-101">Get-AzADSpCredential</span></span>

## <span data-ttu-id="59d72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59d72-102">SYNOPSIS</span></span>
<span data-ttu-id="59d72-103">Ruft eine Liste der Anmeldeinformationen ab, die einem Dienstprinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="59d72-103">Retrieves a list of credentials associated with a service principal.</span></span>

## <span data-ttu-id="59d72-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59d72-104">SYNTAX</span></span>

### <span data-ttu-id="59d72-105">ObjectIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="59d72-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59d72-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="59d72-106">SPNParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59d72-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="59d72-107">DisplayNameParameterSet</span></span>
```
Get-AzADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59d72-108">SPNObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59d72-108">SPNObjectParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="59d72-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="59d72-109">DESCRIPTION</span></span>
<span data-ttu-id="59d72-110">Das Get-AzADSpCredential-Cmdlet kann verwendet werden, um eine Liste der Anmeldeinformationen abzurufen, die einem Dienstprinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="59d72-110">The Get-AzADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="59d72-111">Mit diesem Befehl werden alle Anmeldeinformationseigenschaften (aber nicht der Anmeldeinformationswert) abgerufen, die dem Dienstprinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="59d72-111">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="59d72-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="59d72-112">EXAMPLES</span></span>

### <span data-ttu-id="59d72-113">Beispiel 1 : Listenanmeldeinformationen nach SPN</span><span class="sxs-lookup"><span data-stu-id="59d72-113">Example 1 - List credentials by SPN</span></span>

```
PS C:\> Get-AzADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="59d72-114">Gibt eine Liste der Anmeldeinformationen zurück, die dem Dienstprinzipal mit SPN ' ' zugeordnet http://test12345 sind.</span><span class="sxs-lookup"><span data-stu-id="59d72-114">Returns a list of credentials associated with the service principal with SPN 'http://test12345'.</span></span>

### <span data-ttu-id="59d72-115">Beispiel 2– Listenanmeldeinformationen nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="59d72-115">Example 2 - List credentials by object id</span></span>

```
PS C:\> Get-AzADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

<span data-ttu-id="59d72-116">Gibt eine Liste der Anmeldeinformationen zurück, die dem Dienstprinzipal mit der Objekt-ID "58e28616-99cc-4da4-b705-7672130e1047" zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="59d72-116">Returns a list of credentials associated with the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047".</span></span>

### <span data-ttu-id="59d72-117">Beispiel 3 : Listenanmeldeinformationen durch Piping</span><span class="sxs-lookup"><span data-stu-id="59d72-117">Example 3 - List credentials by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzADSpCredential
```

<span data-ttu-id="59d72-118">Ruft den Dienstprinzipal mit der Objekt-ID "58e28616-99cc-4da4-b705-7672130e1047" ab und gibt ihn an das Get-AzADSpCredential-Cmdlet weiter, um alle Anmeldeinformationen für diesen Dienstprinzipal auflisten.</span><span class="sxs-lookup"><span data-stu-id="59d72-118">Gets the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047" and pipes it to the Get-AzADSpCredential cmdlet to list all credentials for that service principal.</span></span>

## <span data-ttu-id="59d72-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="59d72-119">PARAMETERS</span></span>

### <span data-ttu-id="59d72-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59d72-120">-DefaultProfile</span></span>
<span data-ttu-id="59d72-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="59d72-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59d72-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="59d72-122">-DisplayName</span></span>
<span data-ttu-id="59d72-123">Der Anzeigename des Dienstprinzipals</span><span class="sxs-lookup"><span data-stu-id="59d72-123">The display name of the service principal</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59d72-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="59d72-124">-ObjectId</span></span>
<span data-ttu-id="59d72-125">Die Objekt-ID des Dienstprinzipals zum Abrufen von Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="59d72-125">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59d72-126">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="59d72-126">-ServicePrincipalName</span></span>
<span data-ttu-id="59d72-127">Der Name (SPN) des Dienstprinzipals, aus dem Anmeldeinformationen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="59d72-127">The name (SPN) of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59d72-128">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="59d72-128">-ServicePrincipalObject</span></span>
<span data-ttu-id="59d72-129">Das Dienstprinzipalobjekt zum Abrufen der Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="59d72-129">The service principal object to retrieve the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: SPNObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59d72-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59d72-130">CommonParameters</span></span>
<span data-ttu-id="59d72-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59d72-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59d72-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59d72-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59d72-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="59d72-133">INPUTS</span></span>

### <span data-ttu-id="59d72-134">System.String</span><span class="sxs-lookup"><span data-stu-id="59d72-134">System.String</span></span>

### <span data-ttu-id="59d72-135">Microsoft.Azure.Commands.ActiveDirectory.PSDServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="59d72-135">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="59d72-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="59d72-136">OUTPUTS</span></span>

### <span data-ttu-id="59d72-137">Microsoft.Azure.Commands.ActiveDirectory.PSDCredential</span><span class="sxs-lookup"><span data-stu-id="59d72-137">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="59d72-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="59d72-138">NOTES</span></span>

## <span data-ttu-id="59d72-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="59d72-139">RELATED LINKS</span></span>

[<span data-ttu-id="59d72-140">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="59d72-140">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="59d72-141">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="59d72-141">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="59d72-142">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="59d72-142">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)


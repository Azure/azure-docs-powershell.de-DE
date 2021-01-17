---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
ms.openlocfilehash: c22643c4ce47fc59d2640a6dbbdf9c15b0846f98
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459504"
---
# <span data-ttu-id="f5090-101">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="f5090-101">Get-AzADSpCredential</span></span>

## <span data-ttu-id="f5090-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5090-102">SYNOPSIS</span></span>
<span data-ttu-id="f5090-103">Ruft eine Liste der Anmeldeinformationen ab, die einem Dienstprinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f5090-103">Retrieves a list of credentials associated with a service principal.</span></span>

## <span data-ttu-id="f5090-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f5090-104">SYNTAX</span></span>

### <span data-ttu-id="f5090-105">ObjectIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f5090-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5090-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5090-106">SPNParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f5090-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5090-107">DisplayNameParameterSet</span></span>
```
Get-AzADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5090-108">SPNObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5090-108">SPNObjectParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5090-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f5090-109">DESCRIPTION</span></span>
<span data-ttu-id="f5090-110">Das Get-AzADSpCredential cmdlet kann verwendet werden, um eine Liste der Anmeldeinformationen abzurufen, die einem Dienstprinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f5090-110">The Get-AzADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="f5090-111">Mit diesem Befehl werden alle Anmeldeinformationseigenschaften (aber nicht der Wert für die Anmeldeinformationen) abgerufen, die dem Dienstprinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f5090-111">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="f5090-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f5090-112">EXAMPLES</span></span>

### <span data-ttu-id="f5090-113">Beispiel 1: Auflisten von Anmeldeinformationen nach SPN</span><span class="sxs-lookup"><span data-stu-id="f5090-113">Example 1 - List credentials by SPN</span></span>

```
PS C:\> Get-AzADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="f5090-114">Gibt eine Liste der Anmeldeinformationen zurück, die dem Dienstprinzipal mit SPN ' ' http://test12345 zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f5090-114">Returns a list of credentials associated with the service principal with SPN 'http://test12345'.</span></span>

### <span data-ttu-id="f5090-115">Beispiel 2: Auflisten von Anmeldeinformationen nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="f5090-115">Example 2 - List credentials by object id</span></span>

```
PS C:\> Get-AzADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

<span data-ttu-id="f5090-116">Gibt eine Liste der Anmeldeinformationen zurück, die dem Dienstprinzipal mit der Objekt-ID "58e28616-99cc-4da4-b705-7672130e1047" zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f5090-116">Returns a list of credentials associated with the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047".</span></span>

### <span data-ttu-id="f5090-117">Beispiel 3: Auflisten von Anmeldeinformationen durch Piping</span><span class="sxs-lookup"><span data-stu-id="f5090-117">Example 3 - List credentials by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzADSpCredential
```

<span data-ttu-id="f5090-118">Ruft den Dienstprinzipal mit der Objekt-ID "58e28616-99cc-4da4-b705-7672130e1047" ab und gibt ihn an das cmdlet Get-AzADSpCredential weiter, um alle Anmeldeinformationen für diesen Dienstprinzipal auflisten.</span><span class="sxs-lookup"><span data-stu-id="f5090-118">Gets the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047" and pipes it to the Get-AzADSpCredential cmdlet to list all credentials for that service principal.</span></span>

## <span data-ttu-id="f5090-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5090-119">PARAMETERS</span></span>

### <span data-ttu-id="f5090-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5090-120">-DefaultProfile</span></span>
<span data-ttu-id="f5090-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f5090-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5090-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f5090-122">-DisplayName</span></span>
<span data-ttu-id="f5090-123">Der Anzeigename des Dienstprinzipal</span><span class="sxs-lookup"><span data-stu-id="f5090-123">The display name of the service principal</span></span>

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

### <span data-ttu-id="f5090-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f5090-124">-ObjectId</span></span>
<span data-ttu-id="f5090-125">Die Objekt-ID des Dienstprinzipal, aus dem Anmeldeinformationen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f5090-125">The object id of the service principal to retrieve credentials from.</span></span>

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

### <span data-ttu-id="f5090-126">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="f5090-126">-ServicePrincipalName</span></span>
<span data-ttu-id="f5090-127">Der Name (SPN) des Dienstprinzipal, aus dem Anmeldeinformationen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f5090-127">The name (SPN) of the service principal to retrieve credentials from.</span></span>

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

### <span data-ttu-id="f5090-128">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="f5090-128">-ServicePrincipalObject</span></span>
<span data-ttu-id="f5090-129">Das Dienstprinzipalobjekt, aus dem die Anmeldeinformationen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f5090-129">The service principal object to retrieve the credentials from.</span></span>

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

### <span data-ttu-id="f5090-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5090-130">CommonParameters</span></span>
<span data-ttu-id="f5090-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5090-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5090-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5090-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5090-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f5090-133">INPUTS</span></span>

### <span data-ttu-id="f5090-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f5090-134">System.String</span></span>

### <span data-ttu-id="f5090-135">Microsoft.Azure.Commands.ActiveDirectory.WAHLDServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f5090-135">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="f5090-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f5090-136">OUTPUTS</span></span>

### <span data-ttu-id="f5090-137">Microsoft.Azure.Commands.ActiveDirectory.WERDENDCredential</span><span class="sxs-lookup"><span data-stu-id="f5090-137">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="f5090-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f5090-138">NOTES</span></span>

## <span data-ttu-id="f5090-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f5090-139">RELATED LINKS</span></span>

[<span data-ttu-id="f5090-140">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="f5090-140">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="f5090-141">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="f5090-141">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="f5090-142">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f5090-142">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)


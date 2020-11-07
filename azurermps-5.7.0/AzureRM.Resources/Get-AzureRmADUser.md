---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
ms.openlocfilehash: e111da68e00e0edad54823c763c06f84ea5100e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663442"
---
# <span data-ttu-id="febcd-101">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="febcd-101">Get-AzureRmADUser</span></span>

## <span data-ttu-id="febcd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="febcd-102">SYNOPSIS</span></span>
<span data-ttu-id="febcd-103">Filtert Active Directory-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="febcd-103">Filters active directory users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="febcd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="febcd-104">SYNTAX</span></span>

### <span data-ttu-id="febcd-105">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="febcd-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="febcd-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="febcd-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADUser -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="febcd-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="febcd-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="febcd-108">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="febcd-108">UPNParameterSet</span></span>
```
Get-AzureRmADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="febcd-109">Mailparameterset</span><span class="sxs-lookup"><span data-stu-id="febcd-109">MailParameterSet</span></span>
```
Get-AzureRmADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="febcd-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="febcd-110">DESCRIPTION</span></span>
<span data-ttu-id="febcd-111">Filtert Active Directory-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="febcd-111">Filters active directory users.</span></span>

## <span data-ttu-id="febcd-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="febcd-112">EXAMPLES</span></span>

### <span data-ttu-id="febcd-113">Filtert Benutzer mit UPN</span><span class="sxs-lookup"><span data-stu-id="febcd-113">Filters users using UPN</span></span>
```
PS C:\> Get-AzureRmADUser -UPN foo@domain.com
```

<span data-ttu-id="febcd-114">Ruft den Benutzer mit foo@domain.com</span><span class="sxs-lookup"><span data-stu-id="febcd-114">Gets user with foo@domain.com</span></span>

### <span data-ttu-id="febcd-115">Filtert Benutzer mithilfe der Suchzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="febcd-115">Filters users using Search String</span></span>
```
PS C:\> Get-AzureRmADUser -SearchString Joe
```

<span data-ttu-id="febcd-116">Filtert alle anzeigen Benutzer, die Joe im Anzeigenamen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="febcd-116">Filters all ad users that has Joe in the display name.</span></span>

### <span data-ttu-id="febcd-117">Anzeigen von Benutzern auflisten</span><span class="sxs-lookup"><span data-stu-id="febcd-117">List AD users</span></span>
```
PS C:\> Get-AzureRmADUser
```

<span data-ttu-id="febcd-118">Ruft alle anzeigen Benutzer ab</span><span class="sxs-lookup"><span data-stu-id="febcd-118">Gets all AD users</span></span>

## <span data-ttu-id="febcd-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="febcd-119">PARAMETERS</span></span>

### <span data-ttu-id="febcd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="febcd-120">-DefaultProfile</span></span>
<span data-ttu-id="febcd-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="febcd-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="febcd-122">-Mail</span><span class="sxs-lookup"><span data-stu-id="febcd-122">-Mail</span></span>
```yaml
Type: String
Parameter Sets: MailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="febcd-123">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="febcd-123">-ObjectId</span></span>
<span data-ttu-id="febcd-124">Objekt-ID des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="febcd-124">Object id of the user.</span></span>

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

### <span data-ttu-id="febcd-125">-Search-Funktion</span><span class="sxs-lookup"><span data-stu-id="febcd-125">-SearchString</span></span>
<span data-ttu-id="febcd-126">Der Anzeigename des Benutzers</span><span class="sxs-lookup"><span data-stu-id="febcd-126">The user display name</span></span>

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

### <span data-ttu-id="febcd-127">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="febcd-127">-UserPrincipalName</span></span>
<span data-ttu-id="febcd-128">UPN des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="febcd-128">UPN of the user.</span></span>

```yaml
Type: String
Parameter Sets: EmptyParameterSet
Aliases: UPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="febcd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="febcd-129">CommonParameters</span></span>
<span data-ttu-id="febcd-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="febcd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="febcd-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="febcd-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="febcd-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="febcd-132">INPUTS</span></span>

### <span data-ttu-id="febcd-133">Keine</span><span class="sxs-lookup"><span data-stu-id="febcd-133">None</span></span>
<span data-ttu-id="febcd-134">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="febcd-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="febcd-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="febcd-135">OUTPUTS</span></span>

### <span data-ttu-id="febcd-136">System. Collections. Generic. List ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser]</span><span class="sxs-lookup"><span data-stu-id="febcd-136">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser]</span></span>

## <span data-ttu-id="febcd-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="febcd-137">NOTES</span></span>

## <span data-ttu-id="febcd-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="febcd-138">RELATED LINKS</span></span>

[<span data-ttu-id="febcd-139">Neu – AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="febcd-139">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="febcd-140">Satz-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="febcd-140">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="febcd-141">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="febcd-141">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)


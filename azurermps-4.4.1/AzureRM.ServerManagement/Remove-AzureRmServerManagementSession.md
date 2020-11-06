---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 7476E6DC-6DE6-4199-A680-5717053A8CC5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementSession.md
ms.openlocfilehash: d34678b6ff7996eabf807c92a84d647af15f6a71
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496865"
---
# <span data-ttu-id="50dea-101">Remove-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="50dea-101">Remove-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="50dea-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="50dea-102">SYNOPSIS</span></span>
<span data-ttu-id="50dea-103">Entfernt eine Server Verwaltungssitzung.</span><span class="sxs-lookup"><span data-stu-id="50dea-103">Removes a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50dea-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="50dea-104">SYNTAX</span></span>

### <span data-ttu-id="50dea-105">ByName</span><span class="sxs-lookup"><span data-stu-id="50dea-105">ByName</span></span>
```
Remove-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String>
 [-SessionName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50dea-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="50dea-106">ByObject</span></span>
```
Remove-AzureRmServerManagementSession [[-SessionName] <String>] [-Session] <Session>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50dea-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="50dea-107">DESCRIPTION</span></span>
<span data-ttu-id="50dea-108">Das Cmdlet **Remove-AzureRmServerManagementSession** entfernt eine Azure Server-Verwaltungssitzung.</span><span class="sxs-lookup"><span data-stu-id="50dea-108">The **Remove-AzureRmServerManagementSession** cmdlet removes an Azure Server Management session.</span></span>

## <span data-ttu-id="50dea-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="50dea-109">EXAMPLES</span></span>

## <span data-ttu-id="50dea-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="50dea-110">PARAMETERS</span></span>

### <span data-ttu-id="50dea-111">-Nodename</span><span class="sxs-lookup"><span data-stu-id="50dea-111">-NodeName</span></span>
<span data-ttu-id="50dea-112">Gibt den Namen des Knotens an, auf dem dieses Cmdlet die Sitzung entfernt.</span><span class="sxs-lookup"><span data-stu-id="50dea-112">Specifies the name of the node on which this cmdlet removes the session.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50dea-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50dea-113">-ResourceGroupName</span></span>
<span data-ttu-id="50dea-114">Gibt den Namen der Ressourcengruppe an, zu der die Sitzung gehört.</span><span class="sxs-lookup"><span data-stu-id="50dea-114">Specifies the name of the resource group that the session belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50dea-115">-Sitzung</span><span class="sxs-lookup"><span data-stu-id="50dea-115">-Session</span></span>
<span data-ttu-id="50dea-116">Gibt die vom Cmdlet entfernte Sitzung an.</span><span class="sxs-lookup"><span data-stu-id="50dea-116">Specifies the session that this cmdlet removes.</span></span>

<span data-ttu-id="50dea-117">Dieser Parameter kann anstelle der *ResourceGroupName* -, *NodeName* -und *Sessionname* -Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="50dea-117">This parameter may be used instead of the *ResourceGroupName* , *NodeName* and *SessionName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Session
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50dea-118">-Sitzungsname</span><span class="sxs-lookup"><span data-stu-id="50dea-118">-SessionName</span></span>
<span data-ttu-id="50dea-119">Gibt den Namen der Sitzung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="50dea-119">Specifies the name of the session that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByObject
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50dea-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50dea-120">-DefaultProfile</span></span>
<span data-ttu-id="50dea-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="50dea-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50dea-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50dea-122">CommonParameters</span></span>
<span data-ttu-id="50dea-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50dea-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50dea-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50dea-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50dea-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="50dea-125">INPUTS</span></span>

### <span data-ttu-id="50dea-126">Sitzung</span><span class="sxs-lookup"><span data-stu-id="50dea-126">Session</span></span>
<span data-ttu-id="50dea-127">Der Parameter "Session" akzeptiert den Wert vom Typ "Session" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="50dea-127">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="50dea-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="50dea-128">OUTPUTS</span></span>

## <span data-ttu-id="50dea-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="50dea-129">NOTES</span></span>

## <span data-ttu-id="50dea-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="50dea-130">RELATED LINKS</span></span>

[<span data-ttu-id="50dea-131">Get-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="50dea-131">Get-AzureRmServerManagementSession</span></span>](./Get-AzureRmServerManagementSession.md)

[<span data-ttu-id="50dea-132">Neu – AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="50dea-132">New-AzureRmServerManagementSession</span></span>](./New-AzureRmServerManagementSession.md)



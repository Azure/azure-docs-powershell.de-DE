---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0C806C0A-C199-4AF4-AE2A-11A2467A0873
online version: ''
schema: 2.0.0
ms.openlocfilehash: b11db019a3d7707ce93b2b2355efbaabe77fb91f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006194"
---
# <span data-ttu-id="45b24-101">New-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="45b24-101">New-AzureSBNamespace</span></span>

## <span data-ttu-id="45b24-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="45b24-102">SYNOPSIS</span></span>
<span data-ttu-id="45b24-103">Erstellt einen Namespace.</span><span class="sxs-lookup"><span data-stu-id="45b24-103">Creates a namespace.</span></span>

## <span data-ttu-id="45b24-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="45b24-104">SYNTAX</span></span>

```
New-AzureSBNamespace -Name <String> [-Location <String>] [-CreateACSNamespace <Boolean>]
 -NamespaceType <NamespaceType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="45b24-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="45b24-105">DESCRIPTION</span></span>
<span data-ttu-id="45b24-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="45b24-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="45b24-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="45b24-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="45b24-108">Das Cmdlet **New-AzureSBNamespace** erstellt einen Dienstnamespace für die Verwendung mit Service Bus in Azure.</span><span class="sxs-lookup"><span data-stu-id="45b24-108">The **New-AzureSBNamespace** cmdlet creates a service namespace for use with Service Bus in Azure.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="45b24-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="45b24-109">EXAMPLES</span></span>

### <span data-ttu-id="45b24-110">Beispiel 1: Erstellen eines Dienstnamespace</span><span class="sxs-lookup"><span data-stu-id="45b24-110">Example 1: Create a service namespace</span></span>
```
PS C:\> New-AzureSBNamespace -Name myNameSpace -Location East US 
PS C:\> New-AzureSBNamespace myNameSpace 'East US'
```

<span data-ttu-id="45b24-111">In den Beispielen wird ein Dienstnamespace für die Verwendung mit Service Bus in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="45b24-111">The examples create a service namespace for use with Service Bus in Azure.</span></span>
<span data-ttu-id="45b24-112">Beide Beispiele enthalten die erforderlichen Parameterwerte, aber nur die ersten enthalten die Parameternamen.</span><span class="sxs-lookup"><span data-stu-id="45b24-112">Both examples include the required parameter values, but only the first includes the parameter names.</span></span>
<span data-ttu-id="45b24-113">Das zweite Beispiel kann verwendet werden, da beide Parameter positionsbezogen sind und ihre Werte in der erforderlichen Reihenfolge angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="45b24-113">The second example can be used because both parameters are positional and their values are given in the required order.</span></span>

## <span data-ttu-id="45b24-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="45b24-114">PARAMETERS</span></span>

### <span data-ttu-id="45b24-115">-CreateACSNamespace</span><span class="sxs-lookup"><span data-stu-id="45b24-115">-CreateACSNamespace</span></span>
<span data-ttu-id="45b24-116">Gibt an, ob zusätzlich zum Dienstnamespace ein zugeordneter ACS-Namespace erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="45b24-116">Specifies whether to create an associated ACS namespace in addition to the service namespace.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45b24-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="45b24-117">-Location</span></span>
<span data-ttu-id="45b24-118">Gibt einen Bereich für den neuen Namespace an.</span><span class="sxs-lookup"><span data-stu-id="45b24-118">Specifies a region for the new namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45b24-119">-Name</span><span class="sxs-lookup"><span data-stu-id="45b24-119">-Name</span></span>
<span data-ttu-id="45b24-120">Gibt einen Namen für den neuen Namespace an.</span><span class="sxs-lookup"><span data-stu-id="45b24-120">Specifies a name for the new namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45b24-121">-NamespaceType</span><span class="sxs-lookup"><span data-stu-id="45b24-121">-NamespaceType</span></span>
<span data-ttu-id="45b24-122">Geben Sie an, ob der Namespace für Messaging-oder Benachrichtigungs Hubs verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="45b24-122">Specify a whether to use the namespace for Messaging or Notification Hubs.</span></span>

```yaml
Type: NamespaceType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45b24-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="45b24-123">-Profile</span></span>
<span data-ttu-id="45b24-124">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="45b24-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="45b24-125">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="45b24-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b24-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45b24-126">CommonParameters</span></span>
<span data-ttu-id="45b24-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45b24-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45b24-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45b24-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45b24-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="45b24-129">INPUTS</span></span>

## <span data-ttu-id="45b24-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="45b24-130">OUTPUTS</span></span>

## <span data-ttu-id="45b24-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="45b24-131">NOTES</span></span>

## <span data-ttu-id="45b24-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="45b24-132">RELATED LINKS</span></span>

[<span data-ttu-id="45b24-133">Remove-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="45b24-133">Remove-AzureSBNamespace</span></span>](./Remove-AzureSBNamespace.md)



---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: E771D1F2-A06B-44BB-AAFF-9459DC6303E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 273edfe08e4d2476cd4c1baa2967a829ec1bbcc2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005654"
---
# <span data-ttu-id="acd17-101">Select-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="acd17-101">Select-AzureStorSimpleResource</span></span>

## <span data-ttu-id="acd17-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="acd17-102">SYNOPSIS</span></span>
<span data-ttu-id="acd17-103">Legt eine Ressource als aktuelle Ressource fest.</span><span class="sxs-lookup"><span data-stu-id="acd17-103">Sets a resource as the current resource.</span></span>

## <span data-ttu-id="acd17-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="acd17-104">SYNTAX</span></span>

```
Select-AzureStorSimpleResource -ResourceName <String> [-RegistrationKey <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="acd17-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="acd17-105">DESCRIPTION</span></span>
<span data-ttu-id="acd17-106">Das Cmdlet **Select-AzureStorSimpleResource** legt eine Ressource als aktuelle Ressource fest.</span><span class="sxs-lookup"><span data-stu-id="acd17-106">The **Select-AzureStorSimpleResource** cmdlet sets a resource as the current resource.</span></span>
<span data-ttu-id="acd17-107">Nachdem Sie eine Ressource ausgewählt haben, gelten andere Cmdlets innerhalb dieses Ressourcen Kontexts.</span><span class="sxs-lookup"><span data-stu-id="acd17-107">After you select a resource, other cmdlets apply within that resource context.</span></span>

## <span data-ttu-id="acd17-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="acd17-108">EXAMPLES</span></span>

### <span data-ttu-id="acd17-109">Beispiel 1: Erstmaliges Auswählen einer Ressource</span><span class="sxs-lookup"><span data-stu-id="acd17-109">Example 1: Select a resource for the first time</span></span>
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa" -RegistrationKey "<your registration key>"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

<span data-ttu-id="acd17-110">Dieser Befehl wählt die Ressource mit dem Namen Contoso64-Tsqa als aktuellen Kontext aus.</span><span class="sxs-lookup"><span data-stu-id="acd17-110">This command selects the resource named Contoso64-Tsqa as the current context.</span></span>
<span data-ttu-id="acd17-111">In diesem Beispiel hat der Computer diesen Kontext nicht zuvor initialisiert, und daher müssen Sie einen Wert für den *RegistrationKey* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="acd17-111">In this example, the computer has not had this context initialized previously, and, therefore, you must specify a value for the *RegistrationKey* parameter.</span></span>

### <span data-ttu-id="acd17-112">Beispiel 2: Versuch, eine Ressource auszuwählen</span><span class="sxs-lookup"><span data-stu-id="acd17-112">Example 2: Attempt to select a resource</span></span>
```
This command gets the current context for this computer by using the **Get-AzureStorSimpleResourceContext** cmdlet. The current selected resource is Contoso64-Tsqa. This is consistent with the previous example. 
PS C:\>Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa 

This command attempts to reset the resource to be Contoso02-Resource. For this example, this resource has not been previously selected. The registration key is not saved or included in the command. The command cannot select the resource. 
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso02-Resource"
Select-AzureStorSimpleResource : Could not find the persisted secret. Please use Select-AzureStorSimpleResource and
provide the Registration key once again.
```

### <span data-ttu-id="acd17-113">Beispiel 3: Auswählen einer zuvor ausgewählten Ressource</span><span class="sxs-lookup"><span data-stu-id="acd17-113">Example 3: Select a previously selected resource</span></span>
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

<span data-ttu-id="acd17-114">Dieser Befehl wählt die Ressource mit dem Namen Contoso64-Tsqa als aktuellen Kontext aus.</span><span class="sxs-lookup"><span data-stu-id="acd17-114">This command selects the resource named Contoso64-Tsqa as the current context.</span></span>
<span data-ttu-id="acd17-115">In diesem Beispiel wurde dieser Kontext zuvor ausgewählt, und Sie müssen daher keinen Wert für den *RegistrationKey* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="acd17-115">In this example, that context has previously been selected, and, therefore, you do not need to specify a value for the *RegistrationKey* parameter.</span></span>

## <span data-ttu-id="acd17-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="acd17-116">PARAMETERS</span></span>

### <span data-ttu-id="acd17-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="acd17-117">-Profile</span></span>
<span data-ttu-id="acd17-118">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="acd17-118">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="acd17-119">-RegistrationKey</span><span class="sxs-lookup"><span data-stu-id="acd17-119">-RegistrationKey</span></span>
<span data-ttu-id="acd17-120">Gibt einen Registrierungsschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="acd17-120">Specifies a registration key.</span></span>
<span data-ttu-id="acd17-121">Geben Sie einen Schlüssel an, wenn Sie eine Ressource zum ersten Mal auswählen.</span><span class="sxs-lookup"><span data-stu-id="acd17-121">Specify a key the first time that you select a resource.</span></span>
<span data-ttu-id="acd17-122">Nachdem dieses Cmdlet die aktuelle Ressource ausgewählt hat, verwenden Cmdlets diesen Schlüssel nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="acd17-122">After this cmdlet selects the current resource, cmdlets use this key, as required.</span></span>
<span data-ttu-id="acd17-123">Weitere Informationen finden Sie unter [Abrufen des Dienst Registrierungsschlüssels](https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx)  ( https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx) im Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="acd17-123">For more information, see [Get the service registration key](https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx)  (https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx) on the Microsoft Developer Network.</span></span>

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

### <span data-ttu-id="acd17-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="acd17-124">-ResourceName</span></span>
<span data-ttu-id="acd17-125">Gibt den Namen der Ressource an, die als aktuelle Ressource ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="acd17-125">Specifies the name of the resource to select as the current resource.</span></span>

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

### <span data-ttu-id="acd17-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acd17-126">CommonParameters</span></span>
<span data-ttu-id="acd17-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acd17-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acd17-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acd17-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acd17-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="acd17-129">INPUTS</span></span>

### <span data-ttu-id="acd17-130">Keine</span><span class="sxs-lookup"><span data-stu-id="acd17-130">None</span></span>

## <span data-ttu-id="acd17-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="acd17-131">OUTPUTS</span></span>

### <span data-ttu-id="acd17-132">StorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="acd17-132">StorSimpleResourceContext</span></span>
<span data-ttu-id="acd17-133">Dieses Cmdlet gibt ein **StorSimpleResourceContext** -Objekt zurück, das Details für den Ressourcenkontext enthält.</span><span class="sxs-lookup"><span data-stu-id="acd17-133">This cmdlet returns a **StorSimpleResourceContext** object that contains details for the resource context.</span></span>

## <span data-ttu-id="acd17-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="acd17-134">NOTES</span></span>

## <span data-ttu-id="acd17-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="acd17-135">RELATED LINKS</span></span>

[<span data-ttu-id="acd17-136">Get-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="acd17-136">Get-AzureStorSimpleResource</span></span>](./Get-AzureStorSimpleResource.md)

[<span data-ttu-id="acd17-137">Get-AzureStorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="acd17-137">Get-AzureStorSimpleResourceContext</span></span>](./Get-AzureStorSimpleResourceContext.md)



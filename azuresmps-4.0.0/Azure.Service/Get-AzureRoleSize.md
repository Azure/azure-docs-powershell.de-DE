---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2CBF8DEF-954C-4D9F-B495-C2F76550BC79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35f7e8a7a08ac2793b7e4aeb8615e5fb8fc1f727
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005821"
---
# <span data-ttu-id="3a796-101">Get-AzureRoleSize</span><span class="sxs-lookup"><span data-stu-id="3a796-101">Get-AzureRoleSize</span></span>

## <span data-ttu-id="3a796-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3a796-102">SYNOPSIS</span></span>
<span data-ttu-id="3a796-103">Ruft die Rollengrößen Informationen für das aktuelle Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="3a796-103">Gets the role size information for the current subscription.</span></span>

## <span data-ttu-id="3a796-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a796-104">SYNTAX</span></span>

```
Get-AzureRoleSize [[-InstanceSize] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3a796-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a796-105">DESCRIPTION</span></span>
<span data-ttu-id="3a796-106">Das Cmdlet " **Get-AzureRoleSize** " Ruft die Rollengrößen Informationen für das aktuelle Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="3a796-106">The **Get-AzureRoleSize** cmdlet gets the role size information for the current subscription.</span></span>

## <span data-ttu-id="3a796-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3a796-107">EXAMPLES</span></span>

### <span data-ttu-id="3a796-108">Beispiel 1: Abrufen von Informationen zur Rollengröße</span><span class="sxs-lookup"><span data-stu-id="3a796-108">Example 1: Get role size information</span></span>
```
PS C:\> Get-AzureRoleSize

          InstanceSize               : A6
          RoleSizeLabel              :
          Cores                      : 4
          MemoryInMb                 : 28672
          SupportedByWebWorkerRoles  : True
          SupportedByVirtualMachines : True
          OperationDescription       : Get-AzureRoleSize
          OperationId                : c5ed7b3a-03b3-548d-876b-6688c5b29cce
          OperationStatus            : Succeeded

          InstanceSize               : A7
          RoleSizeLabel              :
          Cores                      : 8
          MemoryInMb                 : 57344
          SupportedByWebWorkerRoles  : True
          SupportedByVirtualMachines : True
          OperationDescription       : Get-AzureRoleSize
          OperationId                : c5ed7b3a-03b3-548d-876b-6688c5b29cce
          OperationStatus            : Succeeded
```

<span data-ttu-id="3a796-109">Dieser Befehl ruft Rollengrößen Informationen für das aktuelle Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="3a796-109">This command gets role size information for the current subscription.</span></span>

### <span data-ttu-id="3a796-110">Beispiel 2: Abrufen von Rollengrößen Informationen und angeben des Rollenformat namens</span><span class="sxs-lookup"><span data-stu-id="3a796-110">Example 2: Get role size information and specify the role size name</span></span>
```
PS C:\> Get-AzureRoleSize -InstanceSize A7

          InstanceSize               : A7
          RoleSizeLabel              :
          Cores                      : 8
          MemoryInMb                 : 57344
          SupportedByWebWorkerRoles  : True
          SupportedByVirtualMachines : True
          OperationDescription       : Get-AzureRoleSize
          OperationId                : c5ed7b3a-03b3-548d-876b-6688c5b29cce
          OperationStatus            : Succeeded
```

<span data-ttu-id="3a796-111">Dieser Befehl ruft Rollengrößen Informationen für die angegebene Rollengröße ab.</span><span class="sxs-lookup"><span data-stu-id="3a796-111">This command gets role size information for the specified role size.</span></span>

### <span data-ttu-id="3a796-112">Beispiel 3: Abrufen von Rollengrößen Informationen für alle virtuellen Computer in allen Azure-Diensten</span><span class="sxs-lookup"><span data-stu-id="3a796-112">Example 3: Get role size information for all virtual machines in all of the Azure services</span></span>
```
PS C:\> Get-AzureService | Get-AzureVM | Get-AzureRoleSize
```

<span data-ttu-id="3a796-113">Dieser Befehl ruft Rollengrößen Informationen für alle virtuellen Computer in allen Azure-Diensten ab.</span><span class="sxs-lookup"><span data-stu-id="3a796-113">This command gets role size information for all virtual machines in all of the Azure services.</span></span>

## <span data-ttu-id="3a796-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a796-114">PARAMETERS</span></span>

### <span data-ttu-id="3a796-115">-Information</span><span class="sxs-lookup"><span data-stu-id="3a796-115">-InformationAction</span></span>
<span data-ttu-id="3a796-116">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="3a796-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3a796-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3a796-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3a796-118">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="3a796-118">Continue</span></span>
- <span data-ttu-id="3a796-119">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="3a796-119">Ignore</span></span>
- <span data-ttu-id="3a796-120">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="3a796-120">Inquire</span></span>
- <span data-ttu-id="3a796-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3a796-121">SilentlyContinue</span></span>
- <span data-ttu-id="3a796-122">Beenden</span><span class="sxs-lookup"><span data-stu-id="3a796-122">Stop</span></span>
- <span data-ttu-id="3a796-123">Anhalten</span><span class="sxs-lookup"><span data-stu-id="3a796-123">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a796-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3a796-124">-InformationVariable</span></span>
<span data-ttu-id="3a796-125">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="3a796-125">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a796-126">-Instanzen</span><span class="sxs-lookup"><span data-stu-id="3a796-126">-InstanceSize</span></span>
<span data-ttu-id="3a796-127">Gibt den Namen der Rollengröße an, beispielsweise: ExtraSmall, klein, groß, Extra Large, A5, A6, A7.</span><span class="sxs-lookup"><span data-stu-id="3a796-127">Specifies the role size name, for example: ExtraSmall, Small, Large, ExtraLarge, A5, A6, A7.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a796-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="3a796-128">-Profile</span></span>
<span data-ttu-id="3a796-129">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="3a796-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3a796-130">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="3a796-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3a796-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a796-131">CommonParameters</span></span>
<span data-ttu-id="3a796-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a796-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a796-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a796-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a796-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3a796-134">INPUTS</span></span>

## <span data-ttu-id="3a796-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3a796-135">OUTPUTS</span></span>

## <span data-ttu-id="3a796-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="3a796-136">NOTES</span></span>

## <span data-ttu-id="3a796-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3a796-137">RELATED LINKS</span></span>

[<span data-ttu-id="3a796-138">Get-AzureRole</span><span class="sxs-lookup"><span data-stu-id="3a796-138">Get-AzureRole</span></span>](./Get-AzureRole.md)

[<span data-ttu-id="3a796-139">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="3a796-139">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="3a796-140">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="3a796-140">Get-AzureVM</span></span>](./Get-AzureVM.md)



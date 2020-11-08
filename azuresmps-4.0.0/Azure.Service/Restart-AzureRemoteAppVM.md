---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: F83D698B-DC48-4ACD-AD2E-4AAECBDA196B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bc8081c9f81305b96b1ac227b9766352ce94b06
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006290"
---
# <span data-ttu-id="8d4ed-101">Restart-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="8d4ed-101">Restart-AzureRemoteAppVM</span></span>

## <span data-ttu-id="8d4ed-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8d4ed-102">SYNOPSIS</span></span>
<span data-ttu-id="8d4ed-103">Startet einen virtuellen Computer in einer Azure RemoteApp-Sammlung neu.</span><span class="sxs-lookup"><span data-stu-id="8d4ed-103">Restarts a virtual machine in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="8d4ed-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d4ed-104">SYNTAX</span></span>

```
Restart-AzureRemoteAppVM -CollectionName <String> -UserUpn <String> [-LogoffMessage <String>]
 [-LogoffWaitSeconds <Int32>] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d4ed-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d4ed-105">DESCRIPTION</span></span>
<span data-ttu-id="8d4ed-106">Mit dem Cmdlet " **Restart-AzureRemoteAppVM** " wird ein virtueller Computer in einer Azure RemoteApp-Sammlung neu gestartet, für die der angegebene Benutzer verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="8d4ed-106">The **Restart-AzureRemoteAppVM** cmdlet restarts a virtual machine in an Azure RemoteApp collection on which the specified user is connected.</span></span>

## <span data-ttu-id="8d4ed-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8d4ed-107">EXAMPLES</span></span>

### <span data-ttu-id="8d4ed-108">Beispiel 1: Erneutes Starten eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="8d4ed-108">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureRemoteAppVM -CollectionName "ContosoVNet" -UserUPN "PattiFuller@contoso.com"
```

<span data-ttu-id="8d4ed-109">Mit diesem Befehl wird ein virtueller Computer in einer Azure RemoteApp-Sammlung mit dem Namen "Contoso" neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="8d4ed-109">This command restarts a virtual machine in an Azure RemoteApp collection named Contoso.</span></span>
<span data-ttu-id="8d4ed-110">Der Benutzer PattiFuller@contoso.com ist mit der Sammlung verbunden, die diesen virtuellen Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="8d4ed-110">The user PattiFuller@contoso.com is connected to the collection which contains this virtual machine.</span></span>

## <span data-ttu-id="8d4ed-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d4ed-111">PARAMETERS</span></span>

### <span data-ttu-id="8d4ed-112">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="8d4ed-112">-CollectionName</span></span>
<span data-ttu-id="8d4ed-113">Gibt den Namen einer Azure RemoteApp-Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="8d4ed-113">Specifies the name of an Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d4ed-114">-LogoffMessage</span><span class="sxs-lookup"><span data-stu-id="8d4ed-114">-LogoffMessage</span></span>
<span data-ttu-id="8d4ed-115">Gibt eine Warnmeldung an, die Benutzern angezeigt wird, die mit dem virtuellen Computer verbunden sind, bevor Sie von diesem Cmdlet abgemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="8d4ed-115">Specifies a warning message shown to users connected to the virtual machine before this cmdlet logs them off.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d4ed-116">-LogoffWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="8d4ed-116">-LogoffWaitSeconds</span></span>
<span data-ttu-id="8d4ed-117">Gibt an, wie lange dieses Cmdlet wartet, bevor es Benutzer abmeldet.</span><span class="sxs-lookup"><span data-stu-id="8d4ed-117">Specifies how long this cmdlet waits before it logs users off.</span></span>
<span data-ttu-id="8d4ed-118">Der Standardwert ist 60 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="8d4ed-118">The default value is 60 seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d4ed-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="8d4ed-119">-Profile</span></span>
<span data-ttu-id="8d4ed-120">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="8d4ed-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8d4ed-121">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="8d4ed-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8d4ed-122">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="8d4ed-122">-UserUpn</span></span>
<span data-ttu-id="8d4ed-123">Gibt den Benutzerprinzipalnamen (User Principal Name, UPN) des Benutzers an, für den das Cmdlet den virtuellen Computer neu startet.</span><span class="sxs-lookup"><span data-stu-id="8d4ed-123">Specifies the user principal name (UPN) of the user for whom this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="8d4ed-124">Verwenden Sie das Cmdlet **Get-AzureRemoteAppVM** , um virtuelle Computer in der Sammlung und verbundenen UPNs zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8d4ed-124">To obtain virtual machines in the collection and connected UPNs, use the **Get-AzureRemoteAppVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d4ed-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8d4ed-125">-Confirm</span></span>
<span data-ttu-id="8d4ed-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8d4ed-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d4ed-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d4ed-127">-WhatIf</span></span>
<span data-ttu-id="8d4ed-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8d4ed-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d4ed-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8d4ed-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d4ed-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d4ed-130">CommonParameters</span></span>
<span data-ttu-id="8d4ed-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d4ed-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d4ed-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d4ed-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d4ed-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8d4ed-133">INPUTS</span></span>

## <span data-ttu-id="8d4ed-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8d4ed-134">OUTPUTS</span></span>

## <span data-ttu-id="8d4ed-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="8d4ed-135">NOTES</span></span>

## <span data-ttu-id="8d4ed-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8d4ed-136">RELATED LINKS</span></span>

[<span data-ttu-id="8d4ed-137">Get-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="8d4ed-137">Get-AzureRemoteAppVM</span></span>](./Get-AzureRemoteAppVM.md)


